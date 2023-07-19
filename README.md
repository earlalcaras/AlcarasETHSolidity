#Installing

# Executing program
// SPDX-License-Identifier: MIT
pragma solidity 0.8.18;
contract GoldCoin {

    // Public variables
    string public tokenName="Tenchi";
    string public tokenAbbrv="Masaki";
    uint public totalSupply=0;

    // Mapping variable 
        mapping(address => uint) public balances;

    // Mint function
    function mint(address recipient, uint value) public {
        totalSupply += value;
        balances[recipient] += value;
    }
    
    // Burn function
function burn(address add, uint val) public {
        if (balances[add] >= val){
        totalSupply -= val;
        balances[add] -= val; 
        }
    }
}
