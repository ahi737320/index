// javascript password generator

"use strict";
var $ = function(id) { return document.getElementById(id); };
var getRandomNumber = function(max) {
var random;
if (!isNaN(max)) {
random = Math.random(); //value >= 0.0 and < 1.0
random = Math.floor(random * max); //value is an integer between 0 and max - 1
random = random + 1; //value is an integer between 1 and max
}
return random;
};
var generatePassword = function() {
$("password").value = ""; // clear previous entry
  
var chars = "0123456789ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz_-+!@";

//Getting number of characters in the chars array
var charsLen = chars.length;

//Fetching the value entered by user
var n = $("num").value;

//Validating the user input
if(isNaN(n))
{
   //If non numeric is entered
   alert(" Sorry!!! Only numbers are allowed... ");
}
else
{
   var i;
   var pwd = "";

   //Iterating for given number of times
   for(i=1; i<=n; i++)
   {
       //Appending a random character each time
       pwd += chars[getRandomNumber(charsLen)];
   }
  
   //Assigning value to password text box
   $("password").value = pwd;
}

};

var clearFields = function() {
$("num").value = "";
$("password").value = "";
$("num").focus();
};
window.onload = function() {
$("generate").onclick = generatePassword;
$("clear").onclick = clearFields;
$("num").focus();
};
