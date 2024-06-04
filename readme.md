# Project Title
Eth final proof

This is the final assesment of Eth proof EVM begineer course . This is a solidity program for storing the details of our coins which stores the tota amount sent by the sender and and store in the function , and another funtion to see whether any loss happen in the process.

## Description

This is a program which is creted in solidity to store the details of our coins which uses the basic concept of solidity like working in remix ethereum and writing a code in .sol file which contains the basics knowledge of solidity like data types , mapping , function demonstrations , and applying condition like if else in solidity . This is a simple program for storing token which will help in future to understand about the basic concept of solidty and runnning the project in . sol file in remix.

## Getting Started


### Executing program

To run this program , i am using Remix , an Solidity IDE.
->To start go to Remix IDE and start coding 
->add a solidity file i named it as myToken.sol 
->include the licence (SPDX) 
->use the latest solidity compiler by including the pragma which will compiler the code using that solidity compiler
->make a contract named mytoken 
->under that contract make public variable 
->create a mapping variable which store address 
->create a function to collect the value of token and add it to the totalamount function
->create a function to take value and analyse the burn occured 
->apply if condition and check if balance is greater than or equal to value then only burn will occur.
->go to solidity compiler which is found on left side of solidity IDE
->click on compile (compilemyToken.sol)
->go to deploy and deploy it.

code blocks for commands
// SPDX-License-Identifier: MIT
pragma solidity 0.8.18;

contract Mytoken {
    // create a public variable
    string public tokenNme = "crypto";
    string public tokenAbbreviation = "crpt";
    uint public totalamount = 0;

    // create a mapping variable
    mapping(address => uint) public balances;

    // create a function for amount collected
    function amountcollection(address _address, uint _value)public{
      totalamount += _value;
      balances[_address]+= _value;
    }

    // create a loss funtion for amount collected
     function loss(address _address, uint _value)public{
      if(balances[_address]>=_value){
      totalamount -= _value;
      balances[_address]+= _value;
      }
    }
}

## Help

Change the compiler solidity version if error occur , then change by going to compiler solidity menu present on left side of the compiler and change the compiler version.

## Authors

->Amrita Kumari

## License

This project is licensed under the MIT License - see the licence file for details.
