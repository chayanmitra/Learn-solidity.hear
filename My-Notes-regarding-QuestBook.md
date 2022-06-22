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


    
