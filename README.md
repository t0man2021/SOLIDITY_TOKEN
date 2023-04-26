# Creating a Token

This Solidity program is a simple program that creates token and demonstrates the mint and burn function of token. The purpose of this program is to show the mint and burn function of a token

## Description

This program is a simple contract written in Solidity, a programming language used for developing smart contracts on the Ethereum blockchain. The contract has a two function that shows the mint, burn function to a token and to get the overall balance. 

## Getting Started

### Executing program

To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., CREAM.sol, SUFFIX.sol, DASH.sol). Copy and paste the following code into the file:
```
// SPDX-License-Identifier: MIT
pragma solidity 0.8.18;

/*
       REQUIREMENTS
    1. Your contract will have public variables that store the details about your coin (Token Name, Token Abbrv., Total Supply)
    2. Your contract will have a mapping of addresses to balances (address => uint)
    3. You will have a mint function that takes two parameters: an address and a value. 
       The function then increases the total supply by that number and increases the balance 
       of the “sender” address by that amount
    4. Your contract will have a burn function, which works the opposite of the mint function, as it will destroy tokens. 
       It will take an address and value just like the mint functions. It will then deduct the value from the total supply 
       and from the balance of the “sender”.
    5. Lastly, your burn function should have conditionals to make sure the balance of "sender" is greater than or equal 
       to the amount that is supposed to be burned.
*/

contract Token {

    // public variables here
   string public tokenName = "CREAM";
   string public tokenAbbrv = "CRM";
   uint public totalSupply = 0;


    // mapping variable here
    mapping(address => uint) public balances;

    // mint function
   function mint (address _address, uint _value) public {
      totalSupply += _value;
      balances[_address] += _value;
   }

    // burn function
   function burn (address _address, uint _value) public {
      if (balances[_address] >= _value) {
          totalSupply -= _value;
          balances[_address] -= _value;
      }
   }
}

```
```
// SPDX-License-Identifier: MIT
pragma solidity 0.8.18;

/*
       REQUIREMENTS
    1. Your contract will have public variables that store the details about your coin (Token Name, Token Abbrv., Total Supply)
    2. Your contract will have a mapping of addresses to balances (address => uint)
    3. You will have a mint function that takes two parameters: an address and a value. 
       The function then increases the total supply by that number and increases the balance 
       of the “sender” address by that amount
    4. Your contract will have a burn function, which works the opposite of the mint function, as it will destroy tokens. 
       It will take an address and value just like the mint functions. It will then deduct the value from the total supply 
       and from the balance of the “sender”.
    5. Lastly, your burn function should have conditionals to make sure the balance of "sender" is greater than or equal 
       to the amount that is supposed to be burned.
*/

contract Token {

    // public variables here
   string public tokenName = "SUFFIX";
   string public tokenAbbrv = "SFX";
   uint public totalSupply = 0;


    // mapping variable here
    mapping(address => uint) public balances;

    // mint function
   function mint (address _address, uint _value) public {
      totalSupply += _value;
      balances[_address] += _value;
   }

    // burn function
   function burn (address _address, uint _value) public {
      if (balances[_address] >= _value) {
          totalSupply -= _value;
          balances[_address] -= _value;
      }
   }
}
```
```
// SPDX-License-Identifier: MIT
pragma solidity 0.8.18;

/*
       REQUIREMENTS
    1. Your contract will have public variables that store the details about your coin (Token Name, Token Abbrv., Total Supply)
    2. Your contract will have a mapping of addresses to balances (address => uint)
    3. You will have a mint function that takes two parameters: an address and a value. 
       The function then increases the total supply by that number and increases the balance 
       of the “sender” address by that amount
    4. Your contract will have a burn function, which works the opposite of the mint function, as it will destroy tokens. 
       It will take an address and value just like the mint functions. It will then deduct the value from the total supply 
       and from the balance of the “sender”.
    5. Lastly, your burn function should have conditionals to make sure the balance of "sender" is greater than or equal 
       to the amount that is supposed to be burned.
*/

contract Token {

    // public variables here
   string public tokenName = "DASH";
   string public tokenAbbrv = "DSH";
   uint public totalSupply = 0;


    // mapping variable here
    mapping(address => uint) public balances;

    // mint function
   function mint (address _address, uint _value) public {
      totalSupply += _value;
      balances[_address] += _value;
   }

    // burn function
   function burn (address _address, uint _value) public {
      if (balances[_address] >= _value) {
          totalSupply -= _value;
          balances[_address] -= _value;
      }
   }
}
```
To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.18" (or another compatible version), and then click on the "Compile CREAM.sol","Compile SUFFIX.sol","Compile DASH.sol" button.

Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the "CREAM","SUFFIX","DASH" contract from the dropdown menu, and then click on the "Deploy" button.

Once the contract is deployed, first get/copy the account number, after that use the mint and click the down arrow then put the account that you copied. Then put any amount that you will mint after that you can interact with it by clicking the transact function. To get the balance click the totalSupply function. After the mint is the burn function, first get/copy the account number, after that use the burn and click the down arrow then put the account that you copied. Then put any amount that you will burn(the amount should'nt be more than you minted) after that you can interact with it by clicking the transact function. then finally to get the balance put the account number and click the balance function to get the latest balance of your acccount.

## Authors

Contributors names and contact info

Todd Harvey Nardo
@t0man#6236(Discord)


## License

This project is licensed under the MIT License - see the LICENSE.md file for details
