## Prompt 1

* URLs cannot have spaces. Instead, all spaces in a string are replaced with %20. Write an algorithm that replaces all spaces in a string with %20.

* You may not use the replace() method or regular expressions to solve this problem. Solve the problem with and without recursion.

* Example

* Input: "Jasmine Ann Jones"

* Output: "Jasmine%20Ann%20Jones"

const input = "Jasmine Ann Jones";
const search = ' ';
const replace = '%20';

const results = input.split(search).join(replace);
<!-- results should be Jasmine%20Ann%20Jones' -->
<!-- can also be done like this: -->
const results = input.split(' ').join('%20');
<!-- as a function -->
const stringToUrl = (string) => {
  result = string.split(' ').join('%20')
}
<!-- as a recursive function -->

const stringToUrl = (string) => {
  let result;
  if string.includes(' ') {
    return string.slice(string.indexOf(' '))
  }
}


<!--  -->
## Prompt 2

* Write an algorithm that removes duplicates from an array. Do not use a function like filter() to solve this. Once you have solved the problem, demonstrate how it can be solved with filter(). Solve the problem with and without recursion.

* Example

* Input: [7, 9, "hi", 12, "hi" 7, 53]

* Output: [7, 9, "hi", 12, 53]
const array = [7, 9, "hi", 12, "hi" 7, 53]

const dupeFilter = (array) => {
  let results = [];
  for (let i = 0; i < array.length; i++) {
    if (results.includes(array[i]) === false) {
      results.push(array[i])
    } else {
      continue
    }
  }
  return results
}

<!-- and recursively -->


## Prompt 3

* Write an algorithm that takes a string with repeated characters and compresses them, using a number to show how many times the repeated character has been compressed. For instance, aaa would be written as 3a. Solve the problem with and without recursion.

* Example

* Input: "aaabccdddda"

* Output: "3ab2c4da"

const stringComp = (string) => {
  if(string.length == 0) {
    console.log('Please enter a valid string')
    return
  }
  let result = '';
  let count = 0;
  for(let i = 0; i < string.lenth; i++) {
    count ++;
    if(string[i] != string[i + 1]) {
      output += string[i] + count;
      count = 0;
    }
  }
  return result;
}

<!-- without counting single letters -->

const stringComp = (string) => {
  if(string.length == 0) {
    console.log('Please enter a valid string')
    return
  }
  let result = '';
  let count = 0;
  for(let i = 0; i < string.lenth; i++) {
    if(string[i] == string[i + 1]) {
      count ++;
    }else if(string[i] != string[i + 1]) {
      if(count == 0) {
        output += string[i];
      }else {
        output += string[i] + count;
      count = 0;
      }
    }
  }
  return result;
}