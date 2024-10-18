# MyFirstToken

This is a simple solidity program written to create a token called MFT. The purpose of the program is to enable the minting of the MFT token and to also give a functionality to burn the token

# Description
This program is a simple contract written in Solidity programming language which is widely used for developing smart contracts on the Ethereum blockchain .It contains a mint function that recieves an address and the value of the number of the token we want minted.It also contains a  burn function which also recieves same parameters as the mint function,but it however burn the recieved value from the total supply if the value do not exceed the total supply.


# Getting Started

To run this program,  go to the Remix website at https://remix.ethereum.org/. which is an online Solidity IDE.
Once on the Remix website, ensure to create a new file by clicking on the "+" icon at the left-hand sidebar. Proceed to Save the file with a .sol extension (e.g., MyFirstToken.sol). Copy and paste the following code into the file:

    // SPDX-License-Identifier: MIT
     pragma solidity 0.8.26;

    contract MyToken{

    // public variables here
    string public tokenName = "MyFirstToken";
    string public tokenAbrv = "MFT";
    uint256 public totalSupply = 0;
    // mapping variable here
    mapping(address => uint256) public balances; 

        // mint function
    function mint(address _address, uint256 _value) public {
        totalSupply += _value;
        balances[_address] += _value;
    }

    // burn function
    function burn(address _address, uint256 _value) public {
        if (balances[_address] >= _value) {
        totalSupply -= _value;
        balances[_address] -= _value;
        }
    } 
    }




Next, ensure you compile the code by clicking on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.4" (or another compatible version), and then click on the "Compile MyFirstToken.sol" button.
After compiling,  deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the "MyFirstToken" contract from the dropdown menu, and then click on the "Deploy" button.

Once the contract is deployed, you can interact with it by calling the mint function and burn function by first copying an address from the "Account" menu under the "Deploy and run transactions" tab
Next on the same "Deploy and run transactions" tab,scroll to the "Deployed Contract" section ,tap on "Mytoken",then insert the address copied ,add a desired value of the token to be minted,then click "transact"

Confirm the token has been minted by clicking on the "Total Supply" button
To call the burn function,repeat the same process,but ensure the value specified is not more than the total supply minted initially.


# Author
https://github.com/Damilola145
