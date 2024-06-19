DESCRIPTION For this assesment we have created a contract on solidity in order fulfil multiple rquirements like:- public variables to store details of coin, 
ie-Token Name,Token Abbreviation,Token Supply mapping of addresses to balances a mint function which takes two parameters: an address and value then increases the total supply 
by that number and increases the balance of the address by that amount. a burn function that destroys tokens by taking an address and value just like the mint functions then deduct 
the value from the total supply and from the balance of the address. Lastly, the burn function should have conditionals to make sure the balance of account is greater than or equal to the 
amount that is supposed to be burned.

Mapping Variable:
balance is initialized as an empty mapping. This will be used to keep track of each address's token balance.
EXECUTION To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.
1-)When the contract MyToken is deployed to the Ethereum blockchain, the following initializations take place:
Public Variables:
Name is set to "Rohan".
Abbrv is set to "RK".
Supply is set to 0.

2-)Mapping of addresses to balances is done by:-mapping(address => uint)public balance;

3-)Mint function:-function mint(address add,uint value)public { Supply += value; balance[add] += value; }
Execution Steps:Increment Supply:
Supply += value;
This increases the total supply of tokens by the amount specified in value.
Update Balance:
balance[add] += value;
This increases the balance of the address add by the amount specified in value.

4-)Condition for burn function:-if(balance[add]>=value)

5-)Burn Function:-function burn(address add,uint value)public { if(balance[add]>=value){ Supply -= value; balance[add] -= value; }
Execution Steps:Check Balance:
if(balance[add] >= value)
This checks if the address add has at least value tokens to burn. If not, the function does nothing.
Decrement Supply:
Supply -= value;
This decreases the total supply of tokens by the amount specified in value.
Update Balance:
balance[add] -= value;
This decreases the balance of the address add by the amount specified in value.

To compile the code we need to click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.18" and then click on the "Compile MyToken.sol" button.
Once the code is compiled, we can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the "MyToken" contract from the dropdown menu, and then 
click on the "Deploy" button. Once the contract is deployed we can run mint and burn functions by clicking on MyToken contract and then clicking on "mint" function and passisng the reqiured 
values like address and value we can run "burn" function in the same way. In order to check value of "Name","Abbrv" and "Supply" we can click on them under "MyToken"
this is how we can can run our code and get the desired output .
