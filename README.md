# MetaCrafters ETH PROOF: Beginner EVM Course Project 
In this repository we will talk about 
"Token Creation with a mapping variable and 2 function (mint and burn) respectively."

## Prerequisites:-

1. [Remix IDE](https://remix.ethereum.org/)  and how to use it.
2. A Little bit knowledge of Solidity

### Code and Explanation:-

1. These lines of code will create a Contract namely "Token" with 3 variables _TokenName , _TokenAbbv and _TotalSupply with values as shown below respectively.

 ```
   contract Token {
    string public _TokenName = "Bake";
    string public _TokenAbbv = "BKE";
    uint public _TotalSupply = 0; }
```
2. Mapping is used to create key - value pair . Over here it will create a mapping variable "balance" which will be used to fetch the amount of token an address is holding.
```
   mapping (address => uint) public balance;
```
3. Over here i have created a mint function which takes 2 parameters address and amt (amount) , upon executing this function the address being passed will have **"amt"** of tokens increased.
```
function mint(address _address , uint _amt) public {
_TotalSupply += _amt;   
balance[_address] += _amt;
}
```
4. Last but not the least burn function which burns certain amount of token from a particular address (both address and amount are passed as parameters) , also an if statement is used because the amount of token you wanna burn must equal to or less than address balance. For ex lets take burn-amt = 100 ; then the address should hold 100 or more than 100.
```
function burn(address _address , uint _amt) public {
if (balance[_address]>=_amt){
_TotalSupply -= _amt;   
balance[_address] -= _amt;
}
```
## Execution 

1. Move on to Remix ide site
2. Paste the code
3. Compile it
4. Deploy through the deployer shown in the left bar
5. Congratulations you have deployed your contract , it will be shown as a pinned contract!

## About me

Hi , My name is Harsh <br />
Currently BE-CSE Student at Chandigarh University <br />
Follow me on [twitter](https://x.com/anharsh100k).



