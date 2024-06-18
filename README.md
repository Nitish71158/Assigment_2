AIM: Create A Token

Discription: Create a contract name as Token in Solidity using ethereum.In this Token pass three variable token name , Abbrv, Total supply after that create one mapping which address to uint which return the token amount that 
address has. After mapping there are two function name as Mint and Burn in mint add amount and retrun total amount and Balanceaddress and in Burn function we decreament the amount in Totalsupply and  in Balanceaddress
include one condition that your amount should be less than or equal to Totalsupply.This program shows how to create a Token in solidity and increase and decrease amount in variable.

Getting Started

Executing Program
To run this program, you can use Remix, an online Solidity IDE.
And run the code.

//Pragma is compiler directive that allows additional information to compiler 
pragma solidity ^0.8.18;

contract MyToken {

    // public variables here
    //Created the three variabl
   string public tokenName = "Iphone";
   string public Abbrv = "Android";
   uint public TotalSupply=0;
    
    // mapping variable here 
mapping(address=>uint) public balances;

    // mint function To add the amount intt toal supply
function mint(address _addr , uint _amount) public{
   TotalSupply += _amount; // total supply increase
   balances[_addr] += _amount; // balance increase
}

    // burn function to decrease value under condition
function Burn(address _addr, uint _amount) public {
    if(TotalSupply>=_amount){// apply condition that amount should be less than or equals to TotalSupply
    TotalSupply -=_amount;//total supply decrease
    balances[_addr] -=_amount; // balance decrease
    }
}

}

Authors
Nitish Kumar Singh
nitishsingh71158@gmail.com
