# ETHEREUM
The Ethereum Virtual Machine, known as EVM, is the name of the computer that Ethereum uses. EVM is, at its core, a single decentralized system.

#  DESCRIPTION
A contract must have public variables for financial data, an address-to-balance mapping, a mint function that increases the total 
supply and the sender's balance, a burn function that eliminates tokens, and a mapping of addresses to balances. A burn function 
that destroys tokens should also be included in the contract. It should be conditioned to ensure that the "sender" balance is more 
than or equal to the sum that was anticipated.

# GETTING STARTED

# EXECUTING PROGRAM
This application may be executed with the usage of a web-based integrated development environment called remix. 
To begin, navigate your browser to the remix website at https://remix.ethereum.org/.  When you go to the website, 
look for a tab on the left side of the page that has a "+" symbol in it. Click that sign to begin a new file.
   
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

# AUTHOR
Earl Francis N. Alcaras - 8213269@ntc.edu.ph
