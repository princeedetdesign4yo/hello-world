# hello-world
//My first application with solidity


// SPDX-License-Identifier: GPL-3.0
pragma solidity >= 0.8.0;

contract HelloWorld {

   string public name;
   string public greetingPrefix = "Hello";

   constructor(string memory initialName) {
      name = initialName;
   }

   function setName(string memory newName) public {
      name = newName;
   }

   function getGreeting() public view returns (string memory) {
      return string(abi.encodePacked(greetingPrefix, name));
   }
}
      
