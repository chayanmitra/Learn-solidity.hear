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
* // SPDX-License-Identifier: MIT    
  
  &emsp; This line indicate the license
* pragma solidity ^0.8.3  
  
  &emsp; This line represents the solidity version used
* contract HelloWorld{}  
  
  &emsp; *contract* defines a class which has it's own Properties and functions that we define. Like here we define the contract HelloWorld which has the property that it greets Good Morning!
* string public greet ="Good Morning!"; *inside {}*
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

```
* function get() public view returns(uint){
        return num;
    }  
    
    &emsp;This function reads the *num* variable and the keywords mean the following:
    * *view* keyword represents a **modifier** that lets the function read the considered state variables, here *num*.
    * *returns(uint)* keyword represents that the function will return a **unsigned integer** (uint) **value** 
    * *public* keyword shows that the function is callable from contracts outside of *contract HelloWorld{}*.
* function set(uint _num) public{
        num = _num;}
    * Observe that the bracket on the right to function *set* is not empty.*set(uint _num)* tells us that the function has *_num* as the parameter which is an **unsigned integer** (uint) **value**.
    * In this function we command the function to update the state variable *num*. We write *_num* into *num*.
