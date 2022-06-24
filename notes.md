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


## Prompt 2