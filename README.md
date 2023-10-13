# My Token

This Solidity program is a simple "My Token" program that demonstrates the basic syntax and functionality of the Solidity programming language. The purpose of this program is to serve as a starting point for those who are new to Solidity and want to get a feel for how it works.

## Getting Started

### How to Run the Program

To run this program, you can use Remix, an online Solidity IDE. Go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., HelloWorld.sol). Copy and paste the following code into the file:

```javascript
pragma solidity 0.8.18;

contract MyToken {

    // public variables here
    string public tokenName = "Valo";
    string public tokenAbbrv = "Rant";
    uint public totalSupply = 0;

    // mapping variable here
    mapping(address => uint) public balances;

    // mint function
    function mint(address _address, uint _value) public{
        totalSupply += _value;
        balances[_address] += _value;
    }

    // burn function
     function burn(address _address, uint _value) public{
        if (balances[_address] >= _value){
            totalSupply -= _value;
            balances[_address] -= _value;
        }
    }
}

```

To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.18" (or another compatible version), and then click on the "Compile MyToken.sol" button.

Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the "MyToken" contract from the dropdown menu, and then click on the "Deploy" button.

Once the contract is deployed, find the deployed contracts. Under Deployed contracts, you will see an arrow, and then click on it. After that, you will see Burn, Mint, balances, token abbrv, token name, and token supply.

Once the deployed contracts is clicked, scroll up to copy the account. To copy, there is a button after the account. After that, paste it in address of burn and mint.

Once you paste the addresses, you can now add value in burn and mint function. Mint is for adding supplies and Burn is for subtracting supplies. After that, you can now run the prorgram and explore how this program works.



## Authors
Kifooo
