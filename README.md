# Functions and Errors

This Program is a simple Error Handling Program that handles require function, assert, and revert function. 

## Error Handling Assessment

This repository is for project assessment and a requirement for the IT Elective 2 subject in BSIT in National Teachers College for the solidity-vax-intermediate course of Metacrafters Academy. The purpose of this project is to enhance my skills in web3. 

## Getting Started
This project aims to tick the three requirements which is the require(), revert(), and assert() functions that stores the data and handling the errors.
### Executing program

To run this program, I used remix.ethereum.org as my IDE to run this project
here's the complete code of my project:

// SPDX-License-Identifier: MIT
pragma solidity >=0.6.12 <0.9.0;

contract MyContract {
    uint256 public value;
    address public owner;

    constructor() {
        owner = msg.sender;
    }

    function setValue(uint256 _newValue) public {


        require(msg.sender == owner, "Only the owner can set the value");

        assert(_newValue != 0);

        if(_newValue < value) {
            revert("New value must be greater than or equal to current value");
        }

        value = _newValue;
    }
}


## Authors

Lacanilao, Jay B. 
@lacanilao_jay @ Discord

## License

This project is licensed under the MIT License - see the LICENSE.md file for details
