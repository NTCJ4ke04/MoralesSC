# MoralesSC
Solidity Version: pragma solidity ^0.8.0; specifies the version of the Solidity compiler to be used. In this case, it indicates that the code is compatible with Solidity version 0.8.0 or higher.
Contract Definition:
contract SimpleContract { ... } defines the contract named SimpleContract. This is the main body of the contract where all the functions and state variables are declared.
State Variables:
address public owner;: This variable stores the address of the owner of the contract.
uint256 public value;: This variable holds an unsigned integer value which can be accessed publicly.
Constructor:
constructor() { ... } is the constructor function. It initializes the owner variable with the address of the account that deployed the contract (msg.sender). This ensures that the deployer of the contract becomes the owner.
External Functions:
setValue(uint256 _newValue) external { ... }: This function allows the owner to set the value of value. It checks if the caller is the owner and ensures that the new value is not zero using require() statements.
getValue() external view returns (uint256) { ... }: This function retrieves the current value of value. It's marked as view because it doesn't modify state variables.
assertExample(uint256 x) external pure returns (uint256) { ... }: This function demonstrates the use of assert(). It checks if the input value x is not zero. If x is zero, the transaction will revert with an internal error.
revertExample() external pure { ... }: This function demonstrates the use of revert(). It simply reverts the transaction with a custom error message.
