# ETHEREUM
The Ethereum Virtual Machine, known as EVM, is the name of the computer that Ethereum uses. EVM is, at its core, a single decentralized system.

#  DESCRIPTION
A contract must have public variables for financial data, an address-to-balance mapping, a mint function that increases the total 
supply and the sender's balance, a burn function that eliminates tokens, and a mapping of addresses to balances. A burn function 
that destroys tokens should also be included in the contract. It should be conditioned to ensure that the "sender" balance is more 
than or equal to the sum that was anticipated.
   
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
