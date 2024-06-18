# ZTOKEN

This Solidity program demonstrates the basic syntax and functionality of the Solidity Programming language. This program aims to establish how to create a simple token simulator with mint and burn functions.

## Description

This program is a simple contract written in Solidity, a programming language used for developing smart contracts on the Ethereum blockchain. The contract has two functions, a mint and a burn. These functions are important in a token. This program serves as a simple introduction to Solidity programming and can be used as a stepping stone for more complex projects in the future.

## Getting Started

### Executing program

You can use Remix, an online Solidity IDE to run this program. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., ZTOKEN.sol). Copy and paste the following code into the file:

```javascript
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.18;
contract MyToken
{
string public tokenName = "ZToken";
string public tokenAbbrv = "ZT"; 
uint public totalSupply = 0;
uint public totalCirculation = 0;

mapping(address => uint) public balances; 

function mint (address _address, uint _value) public
{
totalSupply += _value;
balances[_address] += _value;
totalCirculation += _value;
}

function burn(address _address, uint _value) public 
{
    if(balances[_address] >= _value)
    {
    totalSupply -= _value;
    balances[_address] -= _value;
    totalCirculation -= _value;
    }
}
}

```

To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.4" (or another compatible version), and then click on the "Compile ZTOKEN.sol" button.

Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the "ZTOKEN" contract from the dropdown menu, and then click on the "Deploy" button.

Once the contract is deployed, you can interact with it by transacting with the functions mint and burn. An address will automatically be given by the compiler. Click on the "ZTOKEN" contract in the left-hand sidebar, and then click on the "mint" or "burn" function. Finally, paste the address, enter desired values, and, click on the "transact" button to execute the function that you have chosen. To check if values are entered, select "balances" under mint, paste the address that was used, and, call it. You should see your existing balance. 

## Authors

ZUNIEGA, Kane Nathaniel O. 
## FEU Institute of Technology


## License

This project is licensed under the MIT License - see the LICENSE.md file for details
