![javascript](images/logo-js.png)

# JavaScript Coding Challenges for Beginners

## 1. Multiples of 3 or 5

If we list all the natural numbers below 10 that are multiples of 3 or 5, we get 3, 5, 6 and 9. The sum of these multiples is 23. Finish the solution so that it returns the sum of all the multiples of 3 or 5 below the number passed in.

Note: If the number is a multiple of both 3 and 5, only count it once. Also, if a number is negative, return 0.

```js
const solution = number => {
  // Your solution
};

console.log(solution(0)); // 0
console.log(solution(-15)); // 0
console.log(solution(10)); // 23
console.log(solution(20)); // 78
console.log(solution(200)); // 9168
```

<details><summary>Solution</summary>

```js
const solution = number => {
  let sum = 0;
  for (let i = 3; i < number; i++) {
    if (i % 3 === 0 || i % 5 === 0) {
      sum += i;
    }
  }
  return sum;
};
```

</details>

---

**[⬆ Back to Top](#javascript-coding-challenges-for-beginners)**

## 2. Even or Odd

Create a function that takes an integer as an argument and returns "Even" for even numbers or "Odd" for odd numbers.

```js
const even_or_odd = number => {
  // Your solution
};

console.log(even_or_odd(0)); // 'Even'
console.log(even_or_odd(2)); // 'Even'
console.log(even_or_odd(3)); // 'Odd'
console.log(even_or_odd(-3)); // 'Odd'
```

<details><summary>Solution</summary>

```js
const even_or_odd = number => {
  // Let's use a ternary operator
  return number % 2 === 0 ? 'Even' : 'Odd';
};
```

</details>

---

**[⬆ Back to Top](#javascript-coding-challenges-for-beginners)**

## 3. Clock

The clock shows h hours (0 <= h <= 23), m minutes (0 <= m <= 59) and s seconds (0 <= s <= 59) after midnight. Your task is to write a function which returns the time since midnight in milliseconds. There are 1,000 milliseconds in a second.

```js
const past = (h, m, s) => {
  // Your solution
};

console.log(past(0, 0, 0)); // 0
console.log(past(0, 1, 1)); // 61000
console.log(past(1, 0, 0)); // 3600000
console.log(past(1, 0, 1)); // 3601000
console.log(past(1, 1, 1)); // 3661000
```

<details><summary>Solution</summary>

```js
const past = (h, m, s) => {
  return (h * 60 * 60 + m * 60 + s) * 1000;
};
```

</details>

---

**[⬆ Back to Top](#javascript-coding-challenges-for-beginners)**

## 4. Returning Strings

Write a function that given the input string `name`, returns the greeting statement `Hello, <name> how are you doing today?`

```js
const greet = name => {
  //Your solution
};

console.log(greet('Ryan')); // "Hello, Ryan how are you doing today?"
console.log(greet('Sara')); // "Hello, Sara how are you doing today?"
```

<details><summary>Solution</summary>

```js
const greet = name => {
  // Let's use a template literal
  return `Hello, ${name} how are you doing today?`;
};
```

</details>

---

**[⬆ Back to Top](#javascript-coding-challenges-for-beginners)**

## 5. Century From Year

The first century spans from the year 1 up to and including the year 100, The second - from the year 101 up to and including the year 200, etc. Given a year, return the century it is in.

```js
const century = year => {
  // Your solution
};

console.log(century(1705)); // 18
console.log(century(1900)); // 19
console.log(century(1601)); // 17
console.log(century(2000)); // 20
console.log(century(89)); // 1
```

<details><summary>Solution</summary>

```js
const century = year => {
  return Math.ceil(year / 100);
};
```

</details>

---

**[⬆ Back to Top](#javascript-coding-challenges-for-beginners)**

## 6. Keep Hydrated!

Nathan loves cycling. Because Nathan knows it is important to stay hydrated, he drinks 0.5 litres of water per hour of cycling. Given the time in hours, you need to return the number of litres of water that Nathan will drink, rounded to the smallest value.

```js
const litres = time => {
  // Your solution
};

console.log(litres(0)); // 0
console.log(litres(2)); // 1
console.log(litres(1.4)); // 0
console.log(litres(12.3)); // 6
console.log(litres(0.82)); // 0
console.log(litres(11.8)); // 5
console.log(litres(1787)); // 893
```

<details><summary>Solution</summary>

```js
const litres = time => {
  return Math.floor(time * 0.5);
};
```

</details>

---

**[⬆ Back to Top](#javascript-coding-challenges-for-beginners)**

## 7. Is n Divisible by x and y?

Create a function that checks if a number `n` is divisible by two numbers `x` AND `y`. All inputs are positive, non-zero digits.

```js
const isDivisible = (n, x, y) => {
  // Your solution
};

console.log(isDivisible(3, 3, 4)); // false
console.log(isDivisible(12, 3, 4)); // true
console.log(isDivisible(8, 3, 4)); // false
console.log(isDivisible(48, 3, 4)); // true
```

<details><summary>Solution</summary>

```js
const isDivisible = (n, x, y) => {
  return n % x === 0 && n % y === 0;
};
```

</details>

---

**[⬆ Back to Top](#javascript-coding-challenges-for-beginners)**

## 8. Vowel Count

Return the number (count) of vowels (a, e, i, o, u) in the given string. The input string will only consist of lower case letters and/or spaces.

```js
const getCount = str => {
  // Your solution
};

console.log(getCount('my pyx')); // 0
console.log(getCount('pear tree')); // 4
console.log(getCount('abracadabra')); // 5
console.log(getCount('o a kak ushakov lil vo kashu kakao')); // 13
```

<details><summary>Solution</summary>

```js
const getCount = str => {
  let vowelsCount = 0;
  for (let char of str) {
    if ('aeiou'.includes(char)) vowelsCount++;
  }
  return vowelsCount;
};

// An alternative solution could be to convert the string to an array (using the spread syntax)
// and filtering that array by vowels
const getCount = str => {
  const arr = [...str];
  return arr.filter(ele => ['a', 'e', 'i', 'o', 'u'].includes(ele)).length;
};
```

</details>

---

**[⬆ Back to Top](#javascript-coding-challenges-for-beginners)**

## 9. Disemvowel Trolls

Trolls are attacking your comment section! A common way to deal with this situation is to remove all of the vowels from the trolls' comments, neutralizing the threat. Your task is to write a function that takes a string and returns a new string with all vowels (`a, e, i, o, u`) removed.

```js
const disemvowel = str => {
  // Your solution
};

console.log(disemvowel('This website is for losers LOL!')); // 'Ths wbst s fr lsrs LL!'
```

<details><summary>Solution</summary>

```js
const disemvowel = str => {
  // Let's use regular expressions (regex)
  return str.replace(/[aeiou]/gi, '');
};
```

</details>

---

**[⬆ Back to Top](#javascript-coding-challenges-for-beginners)**

## 10. Find the Odd Int

Given an array of integers, find the one that appears an odd number of times. There will always be only one integer that appears an odd number of times.

```js
const findOdd = arr => {
  // Your solution
};

console.log(findOdd([20, 1, -1, 2, -2, 3, 3, 5, 5, 1, 2, 4, 20, 4, -1, -2, 5])); // 5
console.log(findOdd([20, 1, 1, 2, 2, 3, 3, 5, 5, 4, 20, 4, 5])); // 5
console.log(findOdd([1, 1, 2, -2, 5, 2, 4, 4, -1, -2, 5])); // -1
console.log(findOdd([5, 4, 3, 2, 1, 5, 4, 3, 2, 10, 10])); // 1
console.log(findOdd([1, 1, 1, 1, 1, 1, 10, 1, 1, 1, 1])); // 10
console.log(findOdd([10])); // 10
```

<details><summary>Solution</summary>

```js
const findOdd = arr => {
  return arr.reduce((a, b) => a ^ b);
};
```

</details>

---

**[⬆ Back to Top](#javascript-coding-challenges-for-beginners)**

## 11. Get the Middle Character

Given a word, your job is to return the middle character(s) of the word. If the word's length is odd, return the middle character. If the word's length is even, return the middle 2 characters.

```js
const getMiddle = str => {
  // Your solution
};

console.log(getMiddle('test')); // 'es'
console.log(getMiddle('testing')); // 't'
console.log(getMiddle('middle')); // 'dd'
console.log(getMiddle('A')); // 'A'
```

<details><summary>Solution</summary>

```js
const getMiddle = str => {
  const len = str.length;
  const mid = len / 2;
  // For an odd length, len % 2 equals 1 which is truthy
  return len % 2 ? str[Math.floor(mid)] : str[mid - 1] + str[mid];
};
```

</details>

---

**[⬆ Back to Top](#javascript-coding-challenges-for-beginners)**

## 12. Who likes it?

You probably know the "like" system from Facebook and other social media. People can "like" posts, photos or other items. We want to create the text that should be displayed next to such an item.

Implement a function that takes an input array, containing the names of people who like an item and returns an output string formatted nicely as shown below.

```js
const likes = names => {
  // Your solution
};

console.log(likes([])); // 'no one likes this'
console.log(likes(['Peter'])); // 'Peter likes this'
console.log(likes(['Jacob', 'Alex'])); // 'Jacob and Alex like this'
console.log(likes(['Max', 'John', 'Mark'])); // 'Max, John and Mark like this'
console.log(likes(['Alex', 'Jacob', 'Mark', 'Max'])); // 'Alex, Jacob and 2 others like this'
```

<details><summary>Solution</summary>

```js
const likes = names => {
  const len = names.length;
  let output;
  if (len === 0) {
    output = 'no one likes this';
  } else if (len === 1) {
    output = `${names[0]} likes this`;
  } else if (len === 2) {
    output = `${names[0]} and ${names[1]} like this`;
  } else if (len === 3) {
    output = `${names[0]}, ${names[1]} and ${names[2]} like this`;
  } else {
    output = `${names[0]}, ${names[1]} and ${len - 2} others like this`;
  }

  return output;
};
```

</details>

---

**[⬆ Back to Top](#javascript-coding-challenges-for-beginners)**

## 13. Create Phone Number

Write a function that accepts an array of 10 integers (between 0 and 9), and returns a string of those numbers in the form of a phone number.

```js
const createPhoneNumber = numbers => {
  // Your solution
};

console.log(createPhoneNumber([1, 2, 3, 4, 5, 6, 7, 8, 9, 0])); // '(123) 456-7890'
console.log(createPhoneNumber([1, 1, 1, 1, 1, 1, 1, 1, 1, 1])); // '(111) 111-1111'
console.log(createPhoneNumber([1, 2, 3, 4, 5, 6, 7, 8, 9, 0])); // '(123) 456-7890'
```

<details><summary>Solution</summary>

```js
const createPhoneNumber = numbers => {
  // Using substrings
  const str = numbers.join('');
  return `(${str.substring(0, 3)}) ${str.substring(3, 6)}-${str.substring(6)}`;

  // Alternative solution using RegEx
  // return numbers.join('').replace(/(\d{3})(\d{3})(\d+)/, '($1) $2-$3');

  // Alternative solution using reduce()
  // return numbers.reduce((acc, cur) => acc.replace('x', cur), '(xxx) xxx-xxxx');
};
```

</details>

---

**[⬆ Back to Top](#javascript-coding-challenges-for-beginners)**

## 14. Square Every Digit

Given an integer, your task is to square every digit of it and concatenate them to produce a new integer.

```js
const squareDigits = num => {
  // Your solution
};

console.log(squareDigits(2112)); // 4114
console.log(squareDigits(3212)); // 9414
console.log(squareDigits(9159)); // 8112581
```

<details><summary>Solution</summary>

```js
const squareDigits = num => {
  return Number(
    num
      .toString()
      .split('')
      .map(ele => ele * ele)
      .join('')
  );
};
```

</details>

---

**[⬆ Back to Top](#javascript-coding-challenges-for-beginners)**

## 15. You're a Square!

Write a function that given an integer, checks to see if it is a square number. A square number or perfect square is an integer that is the square of an integer; in other words, it is the product of some integer with itself.

```js
const isSquare = n => {
  // Your solution
};

console.log(isSquare(0)); // true
console.log(isSquare(4)); // true
console.log(isSquare(25)); // true
console.log(isSquare(3)); // false
console.log(isSquare(93)); // false
console.log(isSquare(-1)); // false
```

<details><summary>Solution</summary>

```js
const isSquare = n => {
  return Math.sqrt(n) % 1 === 0;
};
```

</details>

---

**[⬆ Back to Top](#javascript-coding-challenges-for-beginners)**

## 16. Highest and Lowest

Given a string of space-separated numbers, write a function that returns the highest and lowest numbers. There will always be at least one number in the input string.

```js
const highAndLow = numbers => {
  // Your solution
};

console.log(highAndLow('1 2 3 4 5')); // '5 1'
console.log(highAndLow('1 2 -3 4 5')); // '5 -3'
console.log(highAndLow('1 9 3 4 -5')); // '9 -5'
console.log(highAndLow('0 -214 542')); // '542 -214'
```

<details><summary>Solution</summary>

```js
const highAndLow = numbers => {
  const arr = numbers.split(' ');
  return `${Math.max(...arr)} ${Math.min(...arr)}`;
};
```

</details>

---

**[⬆ Back to Top](#javascript-coding-challenges-for-beginners)**

## 17. Descending Order

Write a function that takes any non-negative integer as an argument and returns it with its digits in descending order. Essentially, rearrange the digits to create the highest possible number.

```js
const descendingOrder = n => {
  // Your solution
};

console.log(descendingOrder(0)); // 0
console.log(descendingOrder(1)); // 1
console.log(descendingOrder(1021)); // 2110
console.log(descendingOrder(42145)); // 54421
console.log(descendingOrder(145263)); // 654321
console.log(descendingOrder(123456789)); // 987654321
```

<details><summary>Solution</summary>

```js
const descendingOrder = n => {
  return parseInt(
    n
      .toString()
      .split('')
      .sort((a, b) => b - a)
      .join('')
  );
};
```

</details>

---

**[⬆ Back to Top](#javascript-coding-challenges-for-beginners)**

## 18. Mumbling

Given a string which includes only letters, write a function that produces the outputs below.

```js
const accum = str => {
  // Your solution
};

console.log(accum('abcd')); // 'A-Bb-Ccc-Dddd'
console.log(accum('cwAt')); // 'C-Ww-Aaa-Tttt'
console.log(accum('RqaEzty')); // 'R-Qq-Aaa-Eeee-Zzzzz-Tttttt-Yyyyyyy'
```

<details><summary>Solution</summary>

```js
const accum = str => {
  return str
    .split('')
    .map((ele, index) => ele.toUpperCase() + ele.toLowerCase().repeat(index))
    .join('-');
};
```

</details>

---

**[⬆ Back to Top](#javascript-coding-challenges-for-beginners)**

## 19. Stop gninnipS My sdroW!

Write a function that takes in a string of one or more words, and returns the same string, but with all five or more letter words reversed. Strings passed in will consist of only letters and spaces.

```js
const spinWords = str => {
  // Your solution
};

console.log(spinWords('This is a test')); // 'This is a test'
console.log(spinWords('Hey fellow warriors')); // 'Hey wollef sroirraw'
console.log(spinWords('This is another test')); // 'This is rehtona test'
```

<details><summary>Solution</summary>

```js
const spinWords = str => {
  return str
    .split(' ')
    .map(word => (word.length < 5 ? word : word.split('').reverse().join('')))
    .join(' ');
};
```

</details>

---

**[⬆ Back to Top](#javascript-coding-challenges-for-beginners)**

## 20. Shortest Word

Given a non-empty string of words, return the length of the shortest word(s).

```js
const findShort = str => {
  // Your solution
};

console.log(findShort('Test where final word shortest see')); // 3
console.log(findShort('Lets all go on holiday somewhere very cold')); // 2
console.log(findShort('i want to travel the world writing code one day')); // 1
```

<details><summary>Solution</summary>

```js
const findShort = str => {
  return Math.min(...str.split(' ').map(word => word.length));
};
```

</details>

---

**[⬆ Back to Top](#javascript-coding-challenges-for-beginners)**

## 21. Bit Counting

Write a function that takes an integer as input, and returns the number of bits that are equal to `1` in the binary representation of that number. You can guarantee that input is non-negative. For example the binary representation of `1234` is `10011010010`, so the function should return `5` in this case.

```js
const countBits = n => {
  // Your solution
};

console.log(countBits(0)); // 0
console.log(countBits(4)); // 1
console.log(countBits(7)); // 3
console.log(countBits(9)); // 2
```

<details><summary>Solution</summary>

```js
const countBits = n => {
  return n.toString(2).split('0').join('').length;
};
```

</details>

---

**[⬆ Back to Top](#javascript-coding-challenges-for-beginners)**

## 22. Exes and Ohs

Check to see if a string has the same amount of 'x's and 'o's. The method must return a boolean and be case insensitive. The input string can contain any character.

```js
const XO = str => {
  // Your solution
};

console.log(XO('xo')); // true
console.log(XO('Oo')); // false
console.log(XO('xxOo')); // true
console.log(XO('xxxm')); // false
console.log(XO('ooom')); // false
console.log(XO('ty')); // true (when no 'x' and 'o' is present should return true)
```

<details><summary>Solution</summary>

```js
const XO = str => {
  const lowerStr = str.toLowerCase();
  let result = 0;
  for (const letter of lowerStr) {
    if (letter === 'x') {
      result++;
    } else if (letter === 'o') {
      result--;
    }
  }

  return !result;
};
```

</details>

---

**[⬆ Back to Top](#javascript-coding-challenges-for-beginners)**

## 23. Sum of Positives

Given an array of numbers, write a function that returns the sum of all of the positives ones. If the array is empty, the sum should be `0`.

```js
const positiveSum = arr => {
  // Your solution
};

console.log(positiveSum([1, 2, 3, 4, 5])); // 15
console.log(positiveSum([1, -2, 3, 4, 5])); // 13
console.log(positiveSum([-1, 2, 3, 4, -5])); // 9
console.log(positiveSum([-1, -2, -3, -4, -5])); // 0
console.log(positiveSum([])); // 0
```

<details><summary>Solution</summary>

```js
const positiveSum = arr => {
  return arr.reduce((acc, cur) => (cur > 0 ? acc + cur : acc), 0);
};
```

</details>

---

**[⬆ Back to Top](#javascript-coding-challenges-for-beginners)**

## 24. Find The Parity Outlier

You are given an array of at least length 3 containing integers. The array is either entirely comprised of odd integers or entirely comprised of even integers except for a single integer `N`. Write a function that takes the array as an argument and returns this "outlier" `N`.

```js
const findOutlier = arr => {
  // Your solution
};

console.log(findOutlier([0, 1, 2])); // 1
console.log(findOutlier([1, 2, 3])); // 2
console.log(findOutlier([1, 1, 0, 1, 1])); // 0
console.log(findOutlier([0, 0, 3, 0, 0])); // 3
console.log(findOutlier([160, 3, 1719, 19, 13, -21])); // 160
console.log(findOutlier([4, 0, 100, 4, 11, 2602, 36])); // 11
```

<details><summary>Solution</summary>

```js
const findOutlier = arr => {
  const evenArray = arr.filter(ele => ele % 2 === 0);
  const oddArray = arr.filter(ele => ele % 2 !== 0);
  return evenArray.length === 1 ? evenArray[0] : oddArray[0];
};
```

</details>

---

**[⬆ Back to Top](#javascript-coding-challenges-for-beginners)**

## 25. Array.diff

Write a function that subtracts one list from another and returns the result. It should remove all values from array `a`, which are present in array `b`.

```js
const arrayDiff = (a, b) => {
  // Your solution
};

console.log(arrayDiff([1, 8, 2], [])); // [1, 8, 2]
console.log(arrayDiff([1, 2, 3], [1, 2])); // [3]
console.log(arrayDiff([3, 4], [3])); // [4]
console.log(arrayDiff([], [4, 5])); // []
```

<details><summary>Solution</summary>

```js
const arrayDiff = (a, b) => {
  return a.filter(ele => !b.includes(ele));
};
```

</details>

---

**[⬆ Back to Top](#javascript-coding-challenges-for-beginners)**

## 26. Capitalize Words

Write a function that capitalizes each word in a given input string.

```js
String.prototype.capitalize = function () {
  // Your solution
};

var str = "How can mirrors be real if our eyes aren't real";
console.log(str.capitalize()); // 'How Can Mirrors Be Real If Our Eyes Aren't Real'
```

<details><summary>Solution</summary>

```js
String.prototype.capitalize = function () {
  return this.split(' ')
    .map(ele => ele[0].toUpperCase() + ele.slice(1))
    .join(' ');
};
```

</details>

---

**[⬆ Back to Top](#javascript-coding-challenges-for-beginners)**

## 27. Complementary DNA

DNA is a chemical found in the nucleus of cells and carries the "instructions" for the development and functioning of living organisms. In DNA strings, symbols "A" and "T" are complements of each other, as are "C" and "G". Given one side of the DNA, write a function that returns the other complementary side. The DNA strand is never empty.

```js
const DNAStrand = dna => {
  // Your solution
};

console.log(DNAStrand('AAAA')); // 'TTTT'
console.log(DNAStrand('ATTGC')); // 'TAACG'
console.log(DNAStrand('GTAT')); // 'CATA'
```

<details><summary>Solution</summary>

```js
const DNAStrand = dna => {
  const dnaMap = {
    A: 'T',
    T: 'A',
    G: 'C',
    C: 'G',
  };
  return [...dna].map(ele => dnaMap[ele]).join('');
};
```

</details>

---

**[⬆ Back to Top](#javascript-coding-challenges-for-beginners)**

## 28. Isograms

An isogram is a word that has no repeating letters, consecutive or non-consecutive. Implement a function that determines whether a string that contains only letters is an isogram. Assume the empty string is an isogram. Ignore letter case.

```js
const isIsogram = str => {
  // Your solution
};

console.log(isIsogram('Dermatoglyphics')); // true
console.log(isIsogram('isIsogram')); // false
console.log(isIsogram('isogram')); // true
console.log(isIsogram('moOse')); // false
console.log(isIsogram('aba')); // false
console.log(isIsogram('')); // true
```

<details><summary>Solution</summary>

```js
const isIsogram = str => {
  const lowerStr = str.toLowerCase();

  // Using Set
  return str.length === new Set(lowerStr).size;

  // Alternative solution using every()
  // return [...lowerStr].every((ele, index) => lowerStr.indexOf(ele) === index);
};
```

</details>

---

**[⬆ Back to Top](#javascript-coding-challenges-for-beginners)**

## 29. FizzBuzz

Write a program that prints the numbers from 1 to 100. But for multiples of
`3` prints "Fizz" instead of the number and for the multiples of `5` prints
"Buzz". For numbers which are multiples of both `3` and `5` prints "FizzBuzz".

```js
const fizzBuzz = () => {
  // Your solution
};

fizzBuzz(); // 1, 2, 'Fizz', 4, 'Buzz', 'Fizz', 7, ...
```

<details><summary>Solution</summary>

```js
const fizzBuzz = () => {
  let output;
  for (let num = 1; num <= 100; num++) {
    output = '';
    if (num % 3 === 0) output += 'Fizz';
    if (num % 5 === 0) output += 'Buzz';
    console.log(output || num);
  }
};
```

</details>

---

**[⬆ Back to Top](#javascript-coding-challenges-for-beginners)**

## 30. Counting Duplicates

Write a function that will return the count of distinct case-insensitive alphanumeric characters that occur more than once in the input string.

```js
const duplicateCount = text => {
  // Your solution
};

console.log(duplicateCount('')); // 0
console.log(duplicateCount('abcde')); // 0
console.log(duplicateCount('abA11')); // 2
console.log(duplicateCount('aabbcde')); // 2
console.log(duplicateCount('aabBcde')); // 2
console.log(duplicateCount('Indivisibility')); // 1
console.log(duplicateCount('Indivisibilities')); // 2
```

<details><summary>Solution</summary>

```js
const duplicateCount = text => {
  const lowercaseText = text.toLowerCase();
  let frequency = {};
  let count = 0;

  for (const letter of lowercaseText) {
    frequency[letter] = (frequency[letter] || 0) + 1;
    if (frequency[letter] === 2) count++;
  }
  return count;
};
```

</details>

---

**[⬆ Back to Top](#javascript-coding-challenges-for-beginners)**

## 31. Duplicate Encoder

Write a function that converts a string to a new string where each character in the new string is `(` if that character appears only once in the original string, or `)` if that character appears more than once in the original string. Ignore capitalization when determining if a character is a duplicate.

```js
const duplicateEncode = word => {
  // Your solution
};

console.log(duplicateEncode('din')); // '((('
console.log(duplicateEncode('(( @')); // '))(('
console.log(duplicateEncode('recede')); // '()()()'
console.log(duplicateEncode('Success')); // ')())())'
```

<details><summary>Solution</summary>

```js
const duplicateEncode = word => {
  const lowerWord = word.toLowerCase();
  let result = '';
  for (const char of lowerWord) {
    lowerWord.indexOf(char) !== lowerWord.lastIndexOf(char)
      ? (result += ')')
      : (result += '(');
  }
  return result;
};
```

</details>

---

**[⬆ Back to Top](#javascript-coding-challenges-for-beginners)**

## 32. Reversed Strings

Write a function that reverses the string that is passed to it. For this challenge, you may **NOT** use the JavaScript built-in `reverse()` method.

```js
const reverseString = str => {
  // Your solution
};

console.log(reverseString('hello')); // 'olleh'
console.log(reverseString('world')); // 'dlrow'
console.log(reverseString('')); // ''
console.log(reverseString('h')); // 'h'
```

<details><summary>Solution</summary>

```js
const reverseString = str => {
  let result = '';
  for (let char of str) {
    result = char + result;
  }
  return result;
};
```

</details>

---

**[⬆ Back to Top](#javascript-coding-challenges-for-beginners)**

## 33. Persistent Bugger

Write a function that takes a positive number `num` and returns its multiplicative persistence, which is the number of steps it takes to multiply all the digits of `num` by each other, and repeating with the product until a single digit is obtained.

```js
const persistence = num => {
  // Your solution
};

console.log(persistence(999)); // 4
// because 9*9*9=729, 7*2*9=126, 1*2*6=12, and finally 1*2=2

console.log(persistence(93)); // 3
// because 9*3=27, 2*7=14, 1*4=4 and 4 has only one digit

console.log(persistence(5)); // 0
// because 5 is already a single-digit number
```

<details><summary>Solution</summary>

```js
const persistence = num => {
  if (num < 10) return 0;

  let product = 1;
  while (num >= 10) {
    product *= num % 10;
    num = Math.floor(num / 10);
  }

  // Using recursion
  return 1 + persistence(product * num);
};
```

</details>

---

**[⬆ Back to Top](#javascript-coding-challenges-for-beginners)**

## 34. Fibonacci Number

Fibonacci number (Fibonacci sequence), named after mathematician Fibonacci, is a sequence of numbers that looks like this: `0, 1, 1, 2, 3, 5, 8, 13,...`. You get first two starting numbers, 0 and 1, and the next number in the sequence is always the sum of the previous two numbers.

Write a function `fib()` that takes one parameter `steps`, and returns a number from the Fibonacci sequence, based on the parameter steps, which determines the position in Fibonacci number. For example `fib(0)` returns `0`, `fib(4)` returns `3`, and `fib(15)` returns `610`.

```js
const fib = steps => {
  // Your solution
};

console.log(fib(0)); // 0
console.log(fib(4)); // 3
console.log(fib(17)); // 1597
console.log(fib(20)); // 6765
```

<details><summary>Solution</summary>

```js
// Recursive solution
const fib = steps => {
  if (steps < 2) return steps;
  return fib(steps - 2) + fib(steps - 1);
};
```

</details>

---

**[⬆ Back to Top](#javascript-coding-challenges-for-beginners)**

## 35. Replace with Alphabet Position

Given a string, write a function that replaces every letter with its position in the alphabet: `'a' = 1, 'b' = 2, ...`. If anything in the input isn't a letter, ignore it and don't return it.

```js
const alphabetPosition = text => {
  // Your solution
};

console.log(alphabetPosition('The narwhal bacons at midnight.'));
// '20 8 5 14 1 18 23 8 1 12 2 1 3 15 14 19 1 20 13 9 4 14 9 7 8 20'

console.log(alphabetPosition("The sunset sets at twelve o' clock."));
// '20 8 5 19 21 14 19 5 20 19 5 20 19 1 20 20 23 5 12 22 5 15 3 12 15 3 11'
```

<details><summary>Solution</summary>

```js
const alphabetPosition = text => {
  const startingIndex = 'a'.charCodeAt() - 1;
  return text
    .toLowerCase()
    .match(/[a-z]/g)
    .map(letter => letter.charCodeAt() - startingIndex)
    .join(' ');
};
```

</details>

---

**[⬆ Back to Top](#javascript-coding-challenges-for-beginners)**

## 36. Two Sum

Given an array of integers nums and an integer target, return indices of the two numbers in the array such that they add up to target. You may assume that each input would have exactly one solution, and you may not use the same element twice.

```js
const twoSum = (nums, target) => {
  // Your solution
};

console.log(twoSum([2, 7, 11, 15], 9)); // [0, 1]
console.log(twoSum([3, 2, 4], 6)); // [1, 2]
```

<details><summary>Solution</summary>

```js
const twoSum = (nums, target) => {
  const len = nums.length;
  for (let i = 0; i < len; i++) {
    const j = nums.lastIndexOf(target - nums[i]);
    if (j > i) {
      return [i, j];
    }
  }

  // Alternative solution using Map
  // const map = new Map();

  // for (let i = 0; i < nums.length; i++) {
  //   const otherIndex = map.get(target - nums[i]);
  //   if (typeof otherIndex !== 'undefined') {
  //     return [otherIndex, i];
  //   }
  //   map.set(nums[i], i);
  // }
};
```

</details>

---

**[⬆ Back to Top](#javascript-coding-challenges-for-beginners)**

## 37. Unique In Order

Implement a function that takes an iterable argument (a string or an array) as input and returns a list of items without any elements with the same value next to each other and preserving the original order of elements.

```js
const uniqueInOrder = iterable => {
  // Your solution
};

console.log(uniqueInOrder([1, 2, 2, 3, 3])); // [1, 2, 3]
console.log(uniqueInOrder('ABBCcAD')); // ['A', 'B', 'C', 'c', 'A', 'D']
console.log(uniqueInOrder('AAAABBBCCDAABBB')); // ['A', 'B', 'C', 'D', 'A', 'B']
```

<details><summary>Solution</summary>

```js
const uniqueInOrder = iterable => {
  const arr = [...iterable];
  return arr.filter((ele, index) => ele !== arr[index - 1]);
};
```

</details>

---

**[⬆ Back to Top](#javascript-coding-challenges-for-beginners)**

## 38. Best Time to Buy and Sell Stock

You are given an array `prices` where `prices[i]` is the price of a given stock on the `i`th day. You want to maximize your profit by choosing a single day to buy one stock and choosing a different day in the future to sell that stock. Return the maximum profit you can achieve from this transaction. If you cannot achieve any profit, return `0`.

Example 1:

```shell
Input: prices = [7,1,5,3,6,4]
Output: 5
Explanation: Buy on day 2 (price = 1) and sell on day 5 (price = 6), profit = 6-1 = 5.
Note that buying on day 2 and selling on day 1 is not allowed because you must buy before you sell.
```

Example 2:

```shell
Input: prices = [7,6,4,3,1]
Output: 0
Explanation: In this case, no transactions are done and the max profit = 0.
```

```js
const maxProfit = prices => {
  // Your solution
};

console.log(maxProfit([7, 1, 5, 3, 6, 4])); // 5
console.log(maxProfit([7, 6, 4, 3, 1])); // 0
```

<details><summary>Solution</summary>

```js
const maxProfit = prices => {
  let min = Number.MAX_SAFE_INTEGER;
  let profit = 0;

  for (let i = 0; i < prices.length; i++) {
    min = Math.min(prices[i], min);
    if (prices[i] - min > profit) {
      profit = prices[i] - min;
    }
  }
  return profit;
};
```

</details>

---

**[⬆ Back to Top](#javascript-coding-challenges-for-beginners)**

## 39. Dubstep

Mike works as a DJ in the best London nightclub, and he often uses dubstep music in his performance. Recently, he has decided to take a couple of old songs and make dubstep remixes from them. Let's assume that a song consists of some number of words (that don't contain `WUB`). To make the dubstep remix of this song, Mike inserts a certain number of words `WUB` before the first word of the song (the number may be zero), after the last word (the number may be zero), and between words (at least one between any pair of neighboring words), and then the boy glues together all the words, including `WUB`, in one string and plays the song at the club.

For example, a song with words "I AM X" can transform into a dubstep remix as `WUBWUBIWUBAMWUBWUBX` and cannot transform into `WUBWUBIAMWUBX`.

Recently, Johnny has heard Mike's new dubstep track, but since he isn't into modern music, he decided to find out what was the initial song that Mike remixed. Help Johnny restore the original song.

_Input_: The input consists of a single non-empty string, consisting only of uppercase English letters, the string's length doesn't exceed 200 characters

_Output_: Return the words of the initial song that Mike used to make a dubsteb remix. Separate the words with a space.

```js
const songDecoder = song => {
  // Your solution
};

console.log(songDecoder('AWUBBWUBC'));
// 'A B C' (WUB should be replaced by 1 space)
console.log(songDecoder('AWUBWUBWUBBWUBWUBWUBC'));
// 'A B C' (Multiples WUBs should be replaced by only 1 space)
console.log(songDecoder('WUBAWUBBWUBCWUB'));
// 'A B C' (Any starting or trailing WUBs should be removed)
console.log(songDecoder('WUBWEWUBAREWUBWUBTHEWUBCHAMPIONSWUBMYWUBFRIENDWUB'));
// 'WE ARE THE CHAMPIONS MY FRIEND'
```

<details><summary>Solution</summary>

```js
const songDecoder = song => {
  return song.replace(/(WUB)+/g, ' ').trim();

  // Alternative solution
  // return song.split('WUB').filter(Boolean).join(' ');
};
```

</details>

---

**[⬆ Back to Top](#javascript-coding-challenges-for-beginners)**

## 40. Valid Parentheses

Given a non-empty string `s` containing just the characters `(`, `)`, `{`, `}`, `[`, `]`, determine if the input string is valid. An input string is valid if open brackets are closed by the same type of brackets, and open brackets are closed in the correct order.

```js
const isValid = s => {
  // Your solution
};

console.log(isValid('[')); //false
console.log(isValid('()')); //true
console.log(isValid('(]')); //false
console.log(isValid('{[]}')); //true
console.log(isValid('([)]')); //false
console.log(isValid('()[]{}')); //true
```

<details><summary>Solution</summary>

```js
const isValid = s => {
  const stack = [];
  const pairs = {
    '(': ')',
    '[': ']',
    '{': '}',
  };

  for (const char of s) {
    if (pairs[char]) {
      stack.push(char);
    } else if (pairs[stack.pop()] !== char) {
      return false;
    }
  }
  return !stack.length;
};
```

</details>

---

**[⬆ Back to Top](#javascript-coding-challenges-for-beginners)**

## 41. Reverse Integer

Given a signed 32-bit integer `x`, return `x` with its digits reversed. If reversing `x` causes the value to go outside the signed 32-bit integer range [-2<sup>31</sup>, 2<sup>31</sup> - 1], then return 0.

```js
const reverse = x => {
  // Your solution
};

console.log(reverse(0)); // 0
console.log(reverse(120)); // 21
console.log(reverse(123)); // 321
console.log(reverse(-123)); // -321
console.log(reverse(1534236469)); // 0
```

<details><summary>Solution</summary>

```js
const reverse = x => {
  const MAX = Math.pow(2, 31) - 1;
  const MIN = -1 * Math.pow(2, 31);
  const arr = Math.abs(x).toString().split('');
  const reversed = Math.sign(x) * Number(arr.reverse().join(''));
  return reversed < MIN || reversed > MAX ? 0 : reversed;
};
```

</details>

---

**[⬆ Back to Top](#javascript-coding-challenges-for-beginners)**

## 42. Remove Duplicates from Sorted Array

Given a sorted array `nums`, write a function that removes the duplicates in-place such that each element appears only once and returns the new length. Do **not** allocate extra space for another array, you must do this by modifying the input array in-place with `O(1)` extra memory.

```js
const removeDuplicates = nums => {
  // Your solution
};

console.log(removeDuplicates([1, 1, 2])); // 2 (because [1, 2] has length 2)
console.log(removeDuplicates([0, 1, 1, 1, 2, 2, 3, 3, 4])); // 5
console.log(removeDuplicates([])); // 0
```

<details><summary>Solution</summary>

```js
const removeDuplicates = nums => {
  if (nums.length <= 1) return nums.length;
  let currentIndex = 0;

  for (let i = 1; i < nums.length; i++) {
    if (nums[currentIndex] !== nums[i]) {
      currentIndex++;
      nums[currentIndex] = nums[i];
    }
  }

  nums.length = currentIndex + 1;
  return nums.length;
};
```

</details>

---

**[⬆ Back to Top](#javascript-coding-challenges-for-beginners)**

## 43. Kids With the Greatest Number of Candies

Given an array `candies` where `candies[i]` represents the number of candies that the `i`th kid has, and an integer `extraCandies`, write a function that for each kid checks if he/she would have the greatest number of candies in the group if they were given `extraCandies`. Note that multiple kids can have the greatest number of candies.
For example,

```shell
Input: candies = [2,3,5,1,3], extraCandies = 3
Output: [true,true,true,false,true]

Explanation:
- Kid 1 has 2 candies and if he or she receives all extra candies (3) will have 5 candies --- the greatest number of candies among the kids.
- Kid 2 has 3 candies and if he or she receives at least 2 extra candies will have the greatest number of candies among the kids.
- Kid 3 has 5 candies and this is already the greatest number of candies among the kids.
- Kid 4 has 1 candy and even if he or she receives all extra candies will only have 4 candies.
- Kid 5 has 3 candies and if he or she receives at least 2 extra candies will have the greatest number of candies among the kids.
```

```js
const kidsWithCandies = (candies, extraCandies) => {
  // Your solution
};

console.log(kidsWithCandies([12, 1, 12], 10)); // [true, false, true]
console.log(kidsWithCandies([4, 2, 1, 1, 2], 1)); // [true, false, false, false, false]
```

<details><summary>Solution</summary>

```js
const kidsWithCandies = (candies, extraCandies) => {
  const MAX = Math.max(...candies);
  return candies.map(candy => candy + extraCandies >= MAX);
};
```

</details>

---

**[⬆ Back to Top](#javascript-coding-challenges-for-beginners)**

## 44. Rot13

ROT13 is a simple letter substitution cipher that replaces a letter with the letter 13 letters after it in the alphabet. ROT13 is an example of the Caesar cipher. Create a function that takes a string and returns the string ciphered with Rot13. If there are numbers or special characters included in the string, they should be returned as they are. Only letters from the latin/english alphabet should be shifted.

```js
const rot13 = str => {
  // Your solution
};

console.log(rot13('az AZ')); // nm NM
console.log(rot13('10+2 is twelve.')); // 10+2 vf gjryir.
console.log(rot13('abcdefghijklmnopqrstuvwxyz')); // nopqrstuvwxyzabcdefghijklm
```

<details><summary>Solution</summary>

```js
const rot13 = str => {
  return str.replace(/[a-z]/gi, letter =>
    String.fromCharCode(
      letter.charCodeAt() + (letter.toLowerCase() <= 'm' ? 13 : -13)
    )
  );
};
```

</details>

---

**[⬆ Back to Top](#javascript-coding-challenges-for-beginners)**

## 45. Richest Customer Wealth

You are given an `m x n` integer grid `accounts`, where `accounts[i][j]` is the amount of money the `i`​​​​​​​​​​​th​​​​ customer has in the `j`​​​​​​​​​​​th​​​​ bank. Return the wealth that the richest customer has. A customer's wealth is the amount of money they have in all their bank accounts. The richest customer is the customer that has the maximum wealth. For example:

```shell
Input: accounts = [[1,5],[7,3],[3,5]]
Output: 10
Explanation:
1st customer has wealth = 1 + 5 = 6
2nd customer has wealth = 7 + 3 = 10
3rd customer has wealth = 3 + 5 = 8
The 2nd customer is the richest with a wealth of 10.
```

```js
const maximumWealth = accounts => {
  // Your solution
};

console.log(
  maximumWealth([
    [2, 8, 7],
    [7, 1, 3],
    [1, 9, 5],
  ])
); // 17
console.log(
  maximumWealth([
    [1, 5],
    [7, 3],
    [3, 5],
  ])
); // 10
console.log(
  maximumWealth([
    [1, 2, 3],
    [3, 2, 1],
  ])
); // 6
```

<details><summary>Solution</summary>

```js
const maximumWealth = accounts => {
  return Math.max(
    ...accounts.map(customer => customer.reduce((a, b) => a + b))
  );
};
```

</details>

---

**[⬆ Back to Top](#javascript-coding-challenges-for-beginners)**

## 46. The Hashtag Generator

The marketing team is spending way too much time typing in hashtags. Let's help them with our own Hashtag Generator! Here's the deal:

- It must start with a hashtag `#`.
- Ignore spaces in the input.
- All words must have their first letter capitalized.
- If the final result is longer than 140 chars it must return `false`.
- If the input or the result is an empty string it must return `false`.

```js
const generateHashtag = str => {
  // Your solution
};

console.log(generateHashtag('JavaScript')); // #JavaScript
console.log(generateHashtag('Do we have a Hashtag')); // #DoWeHaveAHashtag
console.log(generateHashtag('    Hello     World   ')); // #HelloWorld
console.log(generateHashtag('coding' + ' '.repeat(140) + 'for life')); // #CodingForLife
console.log(generateHashtag('')); // false
console.log(generateHashtag(' ')); // false
console.log(generateHashtag('a'.repeat(140))); // false
console.log(generateHashtag(' '.repeat(200))); // false
```

<details><summary>Solution</summary>

```js
const generateHashtag = str => {
  const hashtag = str
    .split(' ')
    .reduce(
      (tag, word) => tag + word.charAt(0).toUpperCase() + word.slice(1),
      '#'
    );

  // Alternative solution
  // const hashtag =
  //   '#' +
  //   str
  //     .split(' ')
  //     .map(ele => ele.charAt(0).toUpperCase() + ele.substring(1))
  //     .join('');

  return hashtag.length === 1 || hashtag.length > 140 ? false : hashtag;
};
```

</details>

---

**[⬆ Back to Top](#javascript-coding-challenges-for-beginners)**

## 47. Pete, the Baker

Pete likes to bake some cakes. He has some recipes and ingredients. Unfortunately he is not good in maths. Can you help him to find out, how many cakes he could bake considering his recipes?

Write a function `cakes()`, which takes the `recipe` object and the `available` ingredients object and returns the maximum number of cakes Pete can bake. Ingredients that are not present in the objects, can be considered as `0`.

```js
const cakes = (recipe, available) => {
  // Your solution
};

let recipe = { flour: 500, sugar: 200, eggs: 1 };
let available = { flour: 1200, sugar: 1200, eggs: 5, milk: 200 };
console.log(cakes(recipe, available)); // 2

recipe = { apples: 3, flour: 300, sugar: 150, milk: 100, oil: 100 };
available = { sugar: 500, flour: 2000, milk: 2000 };
console.log(cakes(recipe, available)); // 0
```

<details><summary>Solution</summary>

```js
const cakes = (recipe, available) => {
  let num_cakes = Infinity;
  for (let ingredient in recipe) {
    if (!available[ingredient] || recipe[ingredient] > available[ingredient])
      return 0;
    num_cakes = Math.min(
      num_cakes,
      Math.floor(available[ingredient] / recipe[ingredient])
    );
  }
  return num_cakes;
};
```

</details>

---

**[⬆ Back to Top](#javascript-coding-challenges-for-beginners)**

## 48. Count Characters in Your String

Write a function that counts the frequency of all the characters in a given string.

```js
const count = string => {
  // Your solution
};

console.log(count('')); // {}
console.log(count('aba')); // { a: 2, b: 1 }
```

<details><summary>Solution</summary>

```js
const count = string => {
  const frequency = {};
  for (const char of string) {
    frequency[char] = (frequency[char] || 0) + 1;
  }
  return frequency;
};
```

</details>

---

**[⬆ Back to Top](#javascript-coding-challenges-for-beginners)**

## 49. Break camelCase

Complete the solution so that the function will break up camel casing, using a space between words.

```js
const solution = str => {
  // Your solution
};

console.log(solution('camelCasingHere')); // camel Casing Here
console.log(solution('No Camels here')); // No Camels here
console.log(solution('ABC')); // ABC
console.log(solution('')); // ''
```

<details><summary>Solution</summary>

```js
const solution = str => {
  return str.replace(/([a-z])([A-Z])/g, '$1 $2');
};
```

</details>

---

**[⬆ Back to Top](#javascript-coding-challenges-for-beginners)**

## 50. Check if Word Equals Summation of Two Words

Let's assume that the numeric value of a letter is its position in the alphabet starting from `0` (i.e. `a -> 0, b -> 1, c -> 2`, etc.). Similarly, the numerical value of a string `str` consisting of some lowercase English letters is the concatenation (not sum!) of the numeric values of each letter in `str`, which is then converted into an integer. For example, if `str = 'acb'`, we concatenate each letter's numeric value, resulting in `021` which is then converted to integer `21`.

You are given three strings `firstWord`, `secondWord`, and `targetWord`, each consisting of lowercase English letters `a` through `j` inclusive. Write a function that returns true if the sum of the numerical values of `firstWord` and `secondWord` equals the numerical value of `targetWord`.

```js
const isSumEqual = (firstWord, secondWord, targetWord) => {
  // Your solution
};

console.log(isSumEqual('acb', 'cba', 'cdb')); // true
// The numerical value of firstWord 'acb' is '021' -> 21
// The numerical value of secondWord 'cba' is '210' -> 210
// The numerical value of targetWord 'cdb' is '231' -> 231
// So we return true because 21 + 210 == 231

console.log(isSumEqual('aaa', 'a', 'aab')); // false
// The numerical value of firstWord 'aaa' is '000' -> 0
// The numerical value of secondWord 'a' is '0' -> 0
// The numerical value of targetWord 'aab' is '001' -> 1
// So we return false because 0 + 0 != 1

console.log(isSumEqual('aaa', 'a', 'aaaa')); // true
// The numerical value of firstWord 'aaa' is '000' -> 0
// The numerical value of secondWord 'a' is '0' -> 0
// The numerical value of targetWord 'aaaa' is '0000' -> 0
// So we return true because 0 + 0 == 0
```

<details><summary>Solution</summary>

```js
const getNumericValue = str => {
  const offset = 'a'.charCodeAt();
  const arr = [];

  for (const char of str) {
    arr.push(char.charCodeAt() - offset);
  }

  return parseInt(arr.join(''));
};

const isSumEqual = (firstWord, secondWord, targetWord) => {
  return (
    getNumericValue(firstWord) + getNumericValue(secondWord) ===
    getNumericValue(targetWord)
  );
};
```

</details>

---

**[⬆ Back to Top](#javascript-coding-challenges-for-beginners)**

## 51. Extract the Domain Name From a URL

Write a function that given an input URL, returns its domain name.

```js
const domainName = url => {
  // Your solution
};

console.log(domainName('www.google.ca')); // google
console.log(domainName('http://google.com')); // google
console.log(domainName('https://google.com')); // google
console.log(domainName('http://google.co.jp')); // google
console.log(domainName('https://www.google.com')); // google
```

<details><summary>Solution</summary>

```js
const domainName = url => {
  return url.replace(/(www\.|.*\/\/|\..+)/g, '');
};

// Alternative solution with no regex
// const domainName = url => url.replace('http://', '').replace('https://', '').replace('www.', '').split('.')[0];
```

</details>

---

**[⬆ Back to Top](#javascript-coding-challenges-for-beginners)**

## 52. First Non-repeating Character

Write a function that takes an input string and returns the first character that is not repeated anywhere in the string. Upper- and lowercase letters are considered the same character, but the function should return the correct case for the initial letter.

```js
const firstNonRepeatingLetter = str => {
  // Your solution
};

console.log(firstNonRepeatingLetter('a')); // 'a'
console.log(firstNonRepeatingLetter('stress')); // 't'
console.log(firstNonRepeatingLetter('sTreSS')); // 'T'
console.log(firstNonRepeatingLetter('abba')); // ''
console.log(firstNonRepeatingLetter("Go hang a salami, I'm a lasagna hog!")); // ','
```

<details><summary>Solution</summary>

```js
const firstNonRepeatingLetter = str => {
  const strToLower = str.toLowerCase();
  for (let char of str) {
    if (
      strToLower.indexOf(char.toLowerCase()) ===
      strToLower.lastIndexOf(char.toLowerCase())
    ) {
      return char;
    }
  }
  return '';
};
```

</details>

---

**[⬆ Back to Top](#javascript-coding-challenges-for-beginners)**

## 53. Roman Numerals Encoder

Create a function that takes a positive integer less than `4,000` as its input and returns a string containing the Roman numeral representation of that integer. Modern Roman numerals are written by expressing each digit separately starting with the leftmost digit and skipping any digit with a value of zero. There can't be more than 3 identical symbols in a row. More about Roman numerals: [http://en.wikipedia.org/wiki/Roman_numerals](http://en.wikipedia.org/wiki/Roman_numerals)

Table of individual decimal places for your reference:

|     | Thousands | Hundreds | Tens | Units |
| --- | :-------- | :------- | :--- | :---- |
| 1   | M         | C        | X    | I     |
| 2   | MM        | CC       | XX   | II    |
| 3   | MMM       | CCC      | XXX  | III   |
| 4   |           | CD       | XL   | IV    |
| 5   |           | D        | L    | V     |
| 6   |           | DC       | LX   | VI    |
| 7   |           | DCC      | LXX  | VII   |
| 8   |           | DCCC     | LXXX | VIII  |
| 9   |           | CM       | XC   | IX    |

```js
const convertToRoman = number => {
  // Your solution
};

console.log(convertToRoman(4)); // IV
console.log(convertToRoman(9)); // IX
console.log(convertToRoman(11)); // XI
console.log(convertToRoman(19)); // XIX
console.log(convertToRoman(22)); // XXII
console.log(convertToRoman(15)); // XV
console.log(convertToRoman(39)); // XXX + IX = XXXIX
console.log(convertToRoman(160)); // C + LX = CLX
console.log(convertToRoman(207)); // CC + VII = CCVII
console.log(convertToRoman(246)); // CC + XL + VI = CCXLVI
console.log(convertToRoman(789)); // DCC + LXXX + IX = DCCLXXXIX
console.log(convertToRoman(1009)); // M + IX = MIX
console.log(convertToRoman(1066)); // M + LX + VI = MLXVI
console.log(convertToRoman(1776)); // M + DCC + LXX + VI = MDCCLXXVI
console.log(convertToRoman(1918)); // M + CM + X + VIII = MCMXVIII
console.log(convertToRoman(1954)); // M + CM + L + IV = MCMLIV
console.log(convertToRoman(2014)); // MM + X + IV = MMXIV
console.log(convertToRoman(2421)); // MM + CD + XX + I = MMCDXXI
console.log(convertToRoman(3999)); // MMM + CM + XC + IX = MMMCMXCIX
```

<details><summary>Solution</summary>

```js
const convertToRoman = number => {
  const decimals = [1000, 900, 500, 400, 100, 90, 50, 40, 10, 9, 5, 4, 1];
  // prettier-ignore
  const romans = ['M', 'CM', 'D', 'CD', 'C', 'XC', 'L', 'XL', 'X', 'IX', 'V', 'IV', 'I'];
  let result = '';

  decimals.map((value, index) => {
    while (number >= value) {
      result += romans[index];
      number -= value;
    }
  });

  return result;
};
```

</details>

---

**[⬆ Back to Top](#javascript-coding-challenges-for-beginners)**

## 54. Scramble

Write a function that accepts two strings and returns `true` if some or all of the characters in the first string can be rearranged to match the second string.

```js
const scramble = (str1, str2) => {
  // Your solution
};

console.log(scramble('scriptjava', 'javascript')); // true
console.log(scramble('scriptingjava', 'javascript')); // true
console.log(scramble('scriptsjava', 'javascripts')); // true
console.log(scramble('jscripts', 'javascript')); // false
console.log(scramble('javscripts', 'javascript')); // false
```

<details><summary>Solution</summary>

```js
const scramble = (str1, str2) => {
  return [...str2].every(
    letter => str2.split(letter).length <= str1.split(letter).length
  );

  // Alternative solution
  // const freq = {};
  // for (const letter of str1) {
  //   freq[letter] = (freq[letter] ?? 0) + 1;
  // }

  // for (const letter of str2) {
  //   if (!freq[letter] || freq[letter] < 0) return false;
  //   freq[letter]--;
  // }
  // return true;
};
```

</details>

---

**[⬆ Back to Top](#javascript-coding-challenges-for-beginners)**

## 55. Wave, wAve, waVe, wavE

Write a function that turns a given string into a wave! You will be passed a string and you must return that string in an array where each letter takes turns to become uppercase. The input string will always be lowercase but may be empty. If you encounter a whitespace then pass over it.

```js
const wave = str => {
  // Your solution
};

console.log(wave('hello')); // ['Hello', 'hEllo', 'heLlo', 'helLo', 'hellO'];
console.log(wave(' gap ')); // [' Gap ', ' gAp ', ' gaP '];
console.log(wave('Two words')); // ['Two words', 'tWo words', 'twO words', 'two Words', 'two wOrds', 'two woRds', 'two worDs', 'two wordS'];
```

<details><summary>Solution</summary>

```js
const wave = str => {
  const result = [];
  const len = str.length;
  for (let i = 0; i < len; i++) {
    if (str[i] !== ' ') {
      const word =
        str.substring(0, i).toLowerCase() +
        str[i].toUpperCase() +
        str.substring(i + 1).toLowerCase();
      result.push(word);
    }
  }
  return result;
};
```

</details>

---

**[⬆ Back to Top](#javascript-coding-challenges-for-beginners)**

## 56. Concatenation of Array

Write a function that given an integer array `nums` of length `n`, returns an array of length `2n` where `nums` is concatenated to itself.

```js
const getConcatenation = nums => {
  // Your solution
};

console.log(getConcatenation([1, 2, 3])); // [1, 2, 3, 1, 2, 3]
console.log(getConcatenation([4, 3, 2, 1])); // [4, 3, 2, 1, 4, 3, 2, 1]
```

<details><summary>Solution</summary>

```js
const getConcatenation = nums => {
  return [...nums, ...nums];
};
```

</details>

---

**[⬆ Back to Top](#javascript-coding-challenges-for-beginners)**

## 57. Get Names

Write a function that given an array of users, returns an array of their names. Can you achieve this in one line of code?

```js
const getNames = users => {
  // Your solution
};

const users = [
  {
    id: 001,
    name: 'Alice',
    startDate: '2021-01-03',
  },
  {
    id: 002,
    name: 'Bob',
    startDate: '2020-02-01',
  },
  {
    id: 003,
    name: 'Claire',
    startDate: '2019-03-01',
  },
];

console.log(getNames(users)); // ['Alice', 'Bob', 'Claire']
```

<details><summary>Solution</summary>

```js
const getNames = users => users.map(user => user.name);
```

</details>

---

**[⬆ Back to Top](#javascript-coding-challenges-for-beginners)**

## 58. Object Keys from snake_case to camelCase

Write a function that converts all the keys in an object from snake case to camel case.

```js
const toCamel = obj => {
  // Your solution
};

console.log(
  toCamel({
    first_name: 'John',
    last_name: 'Rambo',
    favorite_movie: 'First Blood',
  })
); // {'firstName': 'John', 'lastName': 'Rambo', 'favoriteMovie': 'First Blood'}
```

<details><summary>Solution</summary>

```js
const toCamel = obj => {
  const result = {};
  for (const [key, value] of Object.entries(obj)) {
    // Let's use regex capture groups
    const camelKey = key.replace(/(_[a-z])/gi, $1 =>
      $1.replace('_', '').toUpperCase()
    );
    result[camelKey] = value;
  }
  return result;
};
```

</details>

---

**[⬆ Back to Top](#javascript-coding-challenges-for-beginners)**

## 59. Valid Palindrome

A phrase is a palindrome if, after converting all uppercase letters into lowercase letters and removing all non-alphanumeric characters, it reads the same forward and backward. Alphanumeric characters include letters and numbers. Given a string `s`, return `true` if it is a palindrome, or `false` otherwise.

```js
const isPalindrome = s => {
  // Your solution
};

console.log(isPalindrome('A man, a plan, a canal: Panama')); // true
// Explanation: "amanaplanacanalpanama" is a palindrome.
console.log(isPalindrome('race a car')); // false
// Explanation: "raceacar" is not a palindrome.
console.log(isPalindrome('ab_a')); // true
// Explanation: "aba" is a palindrome.
console.log(isPalindrome(' ')); // true
// Explanation: `s` is an empty string "" after removing non-alphanumeric characters.
// Since an empty string reads the same forward and backward, it is a palindrome.
```

<details><summary>Solution</summary>

```js
const isPalindrome = s => {
  const str = s.toLowerCase().replace(/[^a-z0-9]/g, '');
  let start = 0;
  let end = str.length - 1;

  while (start < end) {
    if (str[start] !== str[end]) return false;
    start++;
    end--;
  }
  return true;

  // Alternative solution using built-in reverse() method
  // const str = s.toLowerCase().replace(/[^a-z0-9]/g, '');
  // return str === [...str].reverse().join('');
};
```

</details>

---

**[⬆ Back to Top](#javascript-coding-challenges-for-beginners)**

## 60. Move Zeroes

Given an integer array `nums`, move all `0`'s in the array to the end of it while maintaining the relative order of the non-zero elements. Achieve this without copying the array or creating a new array.

```js
const moveZeroes = nums => {
  // Your solution
};

console.log(moveZeroes([0, 1, 0, 3, 12])); // [1, 3, 12, 0, 0]
console.log(moveZeroes([0, 0, 1])); // [1, 0, 0]
console.log(moveZeroes([0])); // [0]
```

<details><summary>Solution</summary>

```js
const moveZeroes = nums => {
  const length = nums.length;
  let index = 0;

  for (let i = 0; i < length; i++) {
    if (nums[i] !== 0) {
      nums[index] = nums[i];
      if (index !== i) {
        nums[i] = 0;
      }
      index++;
    }
  }

  return nums;
};
```

</details>

---

**[⬆ Back to Top](#javascript-coding-challenges-for-beginners)**
