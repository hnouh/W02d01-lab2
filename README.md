## More Problem solving

Remember:

* one step at a time (test thoroughly each step)
* researching a step is excellent (although time-consuming)

# 1
## Calculate the Cube
Write a function `calculateCube` that takes a single number and prints the volume of a cube made from that number.

var i=0
var result=1;
function calculateCube(num){
  while(i<3){
  result=result*num;
  i++;
}
return result;
}

```javascript
console.log(calculateCube(5));
```

> => 125



# 2
## Is a Vowel?
Write a function `isAVowel` that takes a character (i.e. a string of length 1) and returns true if it is a vowel, false otherwise. The vowel could be upper or lower case.

```javascript

> => true

function isAVowel(str){
  var vowel=["a","A","e","E","i","I","u","U","o","O"];
  while(vowel.includes(str)==true){    
    return true;
  }return false;
}

console.log(isAVowel("a"));


# 3
## Get Two Lengths
Write a function `getTwoLengths` that accepts two parameters (strings). The function should return an _array_ of numbers where each number is the length of the corresponding string.


```javascript

function getTwoLengths(str1,str2){

  var result1=0;
  var result2=0;
  var resultArr=[];
  
  var lengthWord1=str1.length;
  var lengthWord2=str2.length;

  while(lengthWord1>=1){
    result1++;
    lengthWord1=lengthWord1-1;
  }

  while(lengthWord2>=1){
    result2++;
    lengthWord2=lengthWord2-1;
  }
  
    resultArr.push(result1);
    resultArr.push(result2);

  return resultArr;
}

console.log(getTwoLengths("Hank", "Hippopopalous"));
```

> => [4, 13]


# 4 
## Get Multiple Lengths

Write a function `getMultipleLengths` that accepts a single parameter as an argument: an **array of strings**. The function should return an array of **numbers** where each number is the length of the corresponding string.


```javascript

function getMultipleLengths(arr){

  var resultArr=[];
  var i=arr.length-1;
  var lengthWord=0;

  while(i>=0){
    lengthWord=arr[i].length;
    resultArr.push(lengthWord);
    i--;
  }
  return resultArr.reverse();
}

console.log(getMultipleLengths(["hello", "what", "is", "up", "dude"]));
```

> => [5, 4, 2, 2, 4]


# 5
## Maximum of Three Numbers
Define a function `maxOfThree` that takes three numbers as arguments and returns the largest of them. If all numbers are the same, it doesn't matter which one is returned. If the two largest numbers are the same, one of them should be returned.

```javascript
function maxOfThree(num1,num2,num3){
var max=0;
while(num1>=num2&&num1>=num3){
max=num1;
return max;
}
while(num2>=num1&&num2>=num3){
max=num2;
return max;
}
while(num3>=num2&&num3>=num1){
max=num3;
return max;
}
}
console.log(maxOfThree(6, 9, 1));
```

> => 9


# 6
## Print Longest Word

Write a function `printLongestWord` that accepts a single argument, an **array of strings**. The method should return the longest word in the array. In case of a tie, the method should return the word that appears first in the array.

```javascript

function printLongestWord(arr){

  var resultArr=[];
  var i=arr.length-1;
  var lengthWord=0;
  var longestWord=0;
  while(i>=0){
    lengthWord=arr[i].length;
    if(lengthWord>=longestWord){
    longestWord=lengthWord;
    resultArr.push(arr[i]);
    }
    i--;
  }   
  resultArr.reverse();
  return resultArr[0]
}

console.log(printLongestWord(["BoJack", "Princess", "Diane", "a", "Max", "Peanutbutter", "big", "blob"]));
```

> => "Peanutbutter"


# 7
## Transmogrify the Numbers
Write a Javascript function called `transmogrify`. This function should accept three arguments, which you can assume will be numbers. Your function should return the "transmogrified" result.

The transmogrified result of three numbers is the product of the first two numbers, raised to the power of the third number.

For example, the transmogrified result of 5, 3, and 2 is `(5 times 3) to the
power of 2` is 225.

```javascript

function transmogrify(num1,num2,num3){
var result=1;
var result2=1;
result=num1*num2;
while(num3>=1){
result2=result2*result;
num3--;
}
return result2;
}

console.log(transmogrify(5, 3, 2));
```

> => 225

<br>
<hr>

# 8
## Project Euler Problem 2
[Project Euler problem #2](https://projecteuler.net/problem=2)

* Write a function that takes a parameter, a number. The function should print the Fibonacci sequence up to that number.

* Adjust the function to push the **even numbered** values into an array.

* Adjust the function to return the summed value of the array.

* Find the sum of the even numbered values that do not exceed four million.

# 9
## A Needle in the Haystack

[From Codewars](https://www.codewars.com/kata/56676e8fabd2d1ff3000000c)

[Join CodeWars](www.codewars.com/r/bEqEeQ)

Can you find the needle in the haystack?

Write a function `findNeedle()` that takes an array full of junk but contains one `"needle"`

After your function finds the needle it should return a message (as a string) that says:

`"found the needle at postition"` plus the index it found the needle so:

`find_needle(['hay', 'junk', 'hay', 'hay', 'moreJunk', 'needle', 'randomJunk'])`

Should return:

`"found the needle at position 5"`
