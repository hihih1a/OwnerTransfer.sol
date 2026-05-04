# OwnerTransfer.sol
OwnerTransfer.sol
pragma solidity ^0.8.20;
contract OwnerTransfer {
    address public owner = msg.sender;

    function transfer(address newOwner) public {
        require(msg.sender == owner);
        owner = newOwner;
    }
}
