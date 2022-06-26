# My Notes Regarding QuestBook
## HelloWorld 
```
// SPDX-License-Identifier: MIT

pragma solidity ^0.8.3;

contract HelloWorld{
    
    string public greet ="Good Morning!";

}
```  
Learnings: 
* ```// SPDX-License-Identifier: MIT```    
  
  &emsp; This line indicate the license
* ```pragma solidity ^0.8.3```  
  
  &emsp; This line represents the solidity version used
* ```contract HelloWorld{}  ```
  
  &emsp; *contract* defines a class which has it's own Properties and functions that we define. Like here we define the contract HelloWorld which has the property that it greets Good Morning!
* ```string public greet ="Good Morning!"; ```
  * *string* is a data type representing text
  * *public* shows that the string is public and it is visible to other contracts outside of HelloWorld
  * *greet* is the string where we store "Good Morning!"

## Read and Write
```
contract HelloWorld{
    
    string public greet ="Good Morning!";
    uint public num=22; 

    function get() public view returns(uint){
        return num;
    }
    function set(uint _num) public{
        num = _num;
}
```
* ```function get() public view returns(uint){return num;}  ```
    
    &emsp;This function reads the *num* variable and the keywords mean the following:
    * *view* keyword represents a **modifier** that lets the function read the considered state variables, here *num*.
    * *returns(uint)* keyword represents that the function will return a **unsigned integer** (uint) **value** 
    * *public* keyword shows that the function is callable from contracts outside of *contract HelloWorld{}*.
* ```function set(uint _num) public{num = _num;}```  
   
   * Observe that the bracket on the right to function *set* is not empty.*set(uint _num)* tells us that the function has *_num* as the parameter which is an **unsigned integer** (uint) **value**.
    * In this function we command the function to update the state variable *num*. We write *_num* into *num*.

## If, else-if, and else conditions
```
contract HelloWorld{
    
    function conditon(uint x) public pure returns(uint){
        if(x<10){
            return 0;
        }else if(x<20){
            return 1;
        }else{
            return 2;
        }

    }
    function ternary(uint _x) public pure returns(uint){
        return _x < 10 ? 1 : 2;
    }
}
```
* ```function conditon(uint x) public pure returns(uint){if(x<10){}```  
    
&emsp; This function returns 0 if x is less than 10, otherwise, returns 1 if x is less than 20, otherwise returns 2.
* *If, else-if, and else* conditions play similarly as in JavaScript.  
``` if(x<10){return 0;}else if(x<20){return 1;}else{return 2;}```
    
* *pure* keyword represents a function modifier which cannot read any state variable from the contract. It can only operate on the parameters of the function.   

* ```function ternary(uint _x) public pure returns(uint){return _x < 10 ? 1 : 2;} ```  
    &emsp; This function returns 1 is _x<10 and 2 if _x> or equal to 10. 
    * Ternary condition is short-hand to if-else condition. 
    * Observe the statement ```return _x < 10 ? 1 : 2;``` which shows that if _x<10 return 1 otherwise return 2.
    * **NOTE:** ```return _x < 10 ? 1 : 2;``` has space after each term.
