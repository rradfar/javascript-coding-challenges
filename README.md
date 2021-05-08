![javascript](images/logo-js.png)

# JavaScript Coding Challenges for Beginners

## 1. Multiples of 3 or 5

If we list all the natural numbers below 10 that are multiples of 3 or 5, we get 3, 5, 6 and 9. The sum of these multiples is 23. Finish the solution so that it returns the sum of all the multiples of 3 or 5 below the number passed in.

Note: If the number is a multiple of both 3 and 5, only count it once. Also, if a number is negative, return 0.

```js
const solution = number => {
  // Your solution
};

console.log(solution(0));   // 0
console.log(solution(-15)); // 0
console.log(solution(10));  // 23
console.log(solution(20));  // 78
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

console.log(even_or_odd(0));  // 'Even'
console.log(even_or_odd(2));  // 'Even'
console.log(even_or_odd(3));  // 'Odd'
console.log(even_or_odd(-3)); // 'Odd'
```

<details><summary>Solution</summary>

```js
const even_or_odd = number => {
  return number % 2 === 0 ? 'Even' : 'Odd';
};
```

</details>

---

**[⬆ Back to Top](#javascript-coding-challenges-for-beginners)**

## 3. Clock

The clock shows h hours (0 <= h <= 23), m minutes (0 <= m <= 59) and s seconds (0 <= s <= 59) after midnight. Your task is to write a function which returns the time since midnight in milliseconds.

```js
const past = (h, m, s) => {
  // Your solution
}

console.log(past(0, 0, 0)); // 0
console.log(past(0, 1, 1)); // 61000
console.log(past(1, 0, 0)); // 3600000
console.log(past(1, 0, 1)); // 3601000
console.log(past(1, 1, 1)); // 3661000
```

<details><summary>Solution</summary>

```js
const past = (h, m, s) => {
  return ((h * 60 * 60) + (m * 60) + s) * 1000;
}
```
</details>

---

**[⬆ Back to Top](#javascript-coding-challenges-for-beginners)**

## 4. Returning Strings

Write a function that given the input string `name`, returns the greeting statement `Hello, <name> how are you doing today?`

```js
const greet = name => {
  //Your solution
}

console.log(greet("Ryan")); // "Hello, Ryan how are you doing today?"
console.log(greet("Sara")); // "Hello, Sara how are you doing today?"
```

<details><summary>Solution</summary>

```js
const greet = name => {
  return `Hello, ${name} how are you doing today?`;
}
```

</details>

---

**[⬆ Back to Top](#javascript-coding-challenges-for-beginners)**

## 5. Century From Year

The first century spans from the year 1 up to and including the year 100, The second - from the year 101 up to and including the year 200, etc. Given a year, return the century it is in.

```js
const century = year => {
  // Your solution
}

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
}
```

</details>

---

**[⬆ Back to Top](#javascript-coding-challenges-for-beginners)**

## 6. Keep Hydrated!

Nathan loves cycling. Because Nathan knows it is important to stay hydrated, he drinks 0.5 litres of water per hour of cycling. You get given the time in hours and you need to return the number of litres Nathan will drink, rounded to the smallest value.

```js
const litres = time => {
  // Your solution
}

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
  return Math.floor(time / 2);
}
```

</details>

---

**[⬆ Back to Top](#javascript-coding-challenges-for-beginners)**

## 7. Is n Divisible by x and y?

Create a function that checks if a number `n` is divisible by two numbers `x` AND `y`. All inputs are positive, non-zero digits.

```js
const isDivisible = (n, x, y) => {
  // Your solution
}

console.log(isDivisible(3, 3, 4)); // false
console.log(isDivisible(12, 3, 4)); // true
console.log(isDivisible(8, 3, 4)); // false
console.log(isDivisible(48, 3, 4)); // true
```

<details><summary>Solution</summary>

```js
const isDivisible = (n, x, y) => {
  return (n % x === 0) && (n % y ===0);
}
```

</details>

---

**[⬆ Back to Top](#javascript-coding-challenges-for-beginners)**

## 8. Vowel Count

Return the number (count) of vowels (a, e, i, o, u) in the given string. The input string will only consist of lower case letters and/or spaces.

```js
const getCount = str => {
  // Your solution
}

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
```

</details>

---

**[⬆ Back to Top](#javascript-coding-challenges-for-beginners)**

## 9. Disemvowel Trolls

Trolls are attacking your comment section! A common way to deal with this situation is to remove all of the vowels from the trolls' comments, neutralizing the threat. Your task is to write a function that takes a string and returns a new string with all vowels (`a, e, i, o, u`) removed.

```js
const disemvowel = str => {
  // Your solution
}

console.log(disemvowel('This website is for losers LOL!')); // 'Ths wbst s fr lsrs LL!'
```

<details><summary>Solution</summary>

```js
const disemvowel = str => {
  return str.replace(/[aeiou]/gi, '');
}
```

</details>

---

**[⬆ Back to Top](#javascript-coding-challenges-for-beginners)**

## 10. Find the Odd Int

Given an array of integers, find the one that appears an odd number of times. There will always be only one integer that appears an odd number of times.

```js
const findOdd = arr => {
  // Your solution
}

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
}
```

</details>

---

**[⬆ Back to Top](#javascript-coding-challenges-for-beginners)**

## 11. Get the Middle Character

Given a word, your job is to return the middle character(s) of the word. If the word's length is odd, return the middle character. If the word's length is even, return the middle 2 characters.

```js
const getMiddle = str => {
  // Your solution
}

console.log(getMiddle('test'));     // 'es'
console.log(getMiddle('testing'));  // 't'
console.log(getMiddle('middle'));   // 'dd'
console.log(getMiddle('A'));        // 'A'
```

<details><summary>Solution</summary>

```js
const getMiddle = str => {
  const midIndex = str.length / 2 ;
  return str.length % 2 ? str[Math.floor(midIndex)] : str[midIndex - 1] + str[midIndex];
}
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
}

console.log(likes([])); // 'no one likes this'
console.log(likes(['Peter'])); // 'Peter likes this'
console.log(likes(['Jacob', 'Alex'])); // 'Jacob and Alex like this'
console.log(likes(['Max', 'John', 'Mark'])); // 'Max, John and Mark like this'
console.log(likes(['Alex', 'Jacob', 'Mark', 'Max'])); // 'Alex, Jacob and 2 others like this'
```

<details><summary>Solution</summary>

```js
const likes = names => {
  let output;
  if (names.length === 0) {
    output = 'no one likes this';
  } else if (names.length === 1) {
    output = `${names[0]} likes this`;
  } else if (names.length === 2) {
    output = `${names[0]} and ${names[1]} like this`;
  } else if (names.length === 3) {
    output = `${names[0]}, ${names[1]} and ${names[2]} like this`;
  } else {
    output = `${names[0]}, ${names[1]} and ${names.length - 2} others like this`;
  }
  return output;
}
```

</details>

---

**[⬆ Back to Top](#javascript-coding-challenges-for-beginners)**

## 13. Create Phone Number

Write a function that accepts an array of 10 integers (between 0 and 9), and returns a string of those numbers in the form of a phone number.

```js
const createPhoneNumber = numbers => {
  // Your solution
}

console.log(createPhoneNumber([1, 2, 3, 4, 5, 6, 7, 8, 9, 0])); // '(123) 456-7890'
console.log(createPhoneNumber([1, 1, 1, 1, 1, 1, 1, 1, 1, 1])); // '(111) 111-1111'
console.log(createPhoneNumber([1, 2, 3, 4, 5, 6, 7, 8, 9, 0])); // '(123) 456-7890'
```

<details><summary>Solution</summary>

```js
const createPhoneNumber = numbers => {
  // Using RegEx
  return numbers.join('').replace(/(\d{3})(\d{3})(\d+)/, '($1) $2-$3');
  
  // Using reduce()
  // return numbers.reduce((acc, cur) => acc.replace('x', cur), '(xxx) xxx-xxxx');
}
```

</details>

---

**[⬆ Back to Top](#javascript-coding-challenges-for-beginners)**

## 14. Square Every Digit

Given an integer, your task is to square every digit of it and concatenate them to produce a new integer.

```js
const squareDigits = num => {
  // Your solution
}

console.log(squareDigits(2112)); // 4114
console.log(squareDigits(3212)); // 9414
console.log(squareDigits(9159)); // 8112581
```

<details><summary>Solution</summary>

```js
const squareDigits = num => {
  return Number(num.toString().split('').map(ele => ele * ele).join(''));
}
```

</details>

---

**[⬆ Back to Top](#javascript-coding-challenges-for-beginners)**

## 15. You're a square!

Write a function that given an integer, checks to see if it is a square number. A square number or perfect square is an integer that is the square of an integer; in other words, it is the product of some integer with itself.

```js
const isSquare = n => {
  // Your solution
};

console.log(isSquare(0));   // true
console.log(isSquare(4));   // true
console.log(isSquare(25));  // true
console.log(isSquare(3));   // false
console.log(isSquare(93));  // false
console.log(isSquare(-1));  // false
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
}

console.log(highAndLow('1 2 3 4 5'));   // '5 1'
console.log(highAndLow('1 2 -3 4 5'));  // '5 -3'
console.log(highAndLow('1 9 3 4 -5'));  // '9 -5'
console.log(highAndLow('0 -214 542'));  // '542 -214'
```

<details><summary>Solution</summary>

```js
const highAndLow = numbers => {
  const arr = numbers.split(' ');
  return `${Math.max(...arr)} ${Math.min(...arr)}`;
}
```

</details>

---

**[⬆ Back to Top](#javascript-coding-challenges-for-beginners)**

## 17. Descending Order

Write a function that takes any non-negative integer as an argument and returns it with its digits in descending order. Essentially, rearrange the digits to create the highest possible number.

```js
const descendingOrder = n => {
  // Your solution
}

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
  return parseInt(n.toString().split('').sort().join(''));
}
```

</details>

---

**[⬆ Back to Top](#javascript-coding-challenges-for-beginners)**

## 18. Mumbling

Given a string which includes only letters, write a function that produces the outputs below.

```js
const accum = str => {
  // Your solution
}

console.log(accum('abcd'));     // 'A-Bb-Ccc-Dddd'
console.log(accum('cwAt'));     // 'C-Ww-Aaa-Tttt'
console.log(accum('RqaEzty'));  // 'R-Qq-Aaa-Eeee-Zzzzz-Tttttt-Yyyyyyy'
```

<details><summary>Solution</summary>

```js
const accum = str => {
  return str.split('').map((ele, index) => ele.toUpperCase() + ele.toLowerCase().repeat(index)).join('-');
}
```

</details>

---

**[⬆ Back to Top](#javascript-coding-challenges-for-beginners)**

## 19. Stop gninnipS My sdroW!

Write a function that takes in a string of one or more words, and returns the same string, but with all five or more letter words reversed. Strings passed in will consist of only letters and spaces.

```js
const spinWords = str => {
  // Your solution
}

console.log(spinWords('This is a test')); // 'This is a test'
console.log(spinWords('Hey fellow warriors')); // 'Hey wollef sroirraw'
console.log(spinWords('This is another test')); // 'This is rehtona test'
```

<details><summary>Solution</summary>

```js
const spinWords = str => {
  return str.split(' ').map(word => word.length < 5 ? word : word.split('').reverse().join('')).join(' ');
}
```

</details>

---

**[⬆ Back to Top](#javascript-coding-challenges-for-beginners)**

## 20. Shortest Word

Given a non-empty string of words, return the length of the shortest word(s).

```js
const findShort = str => {
  // Your solution
}

console.log(findShort("Test where final word shortest see")); // 3
console.log(findShort("Lets all go on holiday somewhere very cold")); // 2
console.log(findShort("i want to travel the world writing code one day")); // 1
```

<details><summary>Solution</summary>

```js
const findShort = str => {
  return Math.min(...str.split(' ').map(word => word.length));
}
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
}

console.log(XO('xo')); // true
console.log(XO('Oo')); // false
console.log(XO('xxOo')); // true
console.log(XO('xxxm')); // false
console.log(XO('ooom')); // false
console.log(XO("ty")); // true (when no 'x' and 'o' is present should return true)
```

<details><summary>Solution</summary>

```js
const XO = str => {
  let result = 0;
  for (let letter of str.toLowerCase()) {
    if (letter === 'x') {
      result++;
    } else if (letter === 'o') {
      result--;
    }
  }
  return !result;
}
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
  return arr.filter(ele => ele > 0).reduce((a, b) => a + b, 0);
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
  const even = arr.filter(ele => ele % 2 === 0);
  const odd = arr.filter(ele => ele % 2 !== 0);
  return even.length === 1 ? even[0] : odd[0];
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

console.log(arrayDiff([1,8,2], []));    // [1, 8, 2]
console.log(arrayDiff([1,2,3], [1,2])); // [3]
console.log(arrayDiff([3,4], [3]));     // [4]
console.log(arrayDiff([], [4,5]));      // []
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
  return this.split(' ').map(ele => ele[0].toUpperCase() + ele.slice(1)).join(' ');
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
}

console.log(DNAStrand('AAAA'));   // 'TTTT'
console.log(DNAStrand('ATTGC'));  // 'TAACG'
console.log(DNAStrand('GTAT'));   // 'CATA'
```

<details><summary>Solution</summary>

```js
const DNAStrand = dna => {
  const MAP = {
    'A': 'T',
    'T': 'A',
    'G': 'C',
    'C': 'G',
  }
  return [...dna].map(ele => MAP[ele]).join('');
}
```

</details>

---

**[⬆ Back to Top](#javascript-coding-challenges-for-beginners)**

## 28. Isograms

An isogram is a word that has no repeating letters, consecutive or non-consecutive. Implement a function that determines whether a string that contains only letters is an isogram. Assume the empty string is an isogram. Ignore letter case.

```js
const isIsogram = str => {
  // Your solution
}

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
  return str.length === new Set(str.toLowerCase()).size;
}
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
}

fizzBuzz(); // 1, 2, 'Fizz', 4, 'Buzz', 'Fizz', 7, ...
```

<details><summary>Solution</summary>

```js
const fizzBuzz = () => {
  let result;
  for (let i = 1; i <= 100; i++) {
    result = '';
    if (i % 3 === 0) result += 'Fizz';
    if (i % 5 === 0) result += 'Buzz';
    console.log(result || i);
  }
}
```

</details>

---

**[⬆ Back to Top](#javascript-coding-challenges-for-beginners)**

## 30. Counting Duplicates

Write a function that will return the count of distinct case-insensitive alphanumeric characters that occur more than once in the input string.

```js
const duplicateCount = text => {
  // Your solution
}

console.log(duplicateCount("")); // 0
console.log(duplicateCount("abcde")); // 0
console.log(duplicateCount("aabbcde")); // 2
console.log(duplicateCount("aabBcde")); // 2, "should ignore case"
console.log(duplicateCount("Indivisibility")); // 1
console.log(duplicateCount("Indivisibilities")); // 2, "characters may not be adjacent"
```

<details><summary>Solution</summary>

```js
const duplicateCount = text => {
  text = text.toLowerCase();
  const freq = {};
  for (let letter of text) {
    freq[letter] = (freq[letter] || 0) + 1;
  }
  
  let result = 0;
  for (let letter in freq) {
    if (freq[letter] > 1) result++;
  }
  return result;
}
```

</details>

---

**[⬆ Back to Top](#javascript-coding-challenges-for-beginners)**

## 31. Duplicate Encoder

Write a function that converts a string to a new string where each character in the new string is `(` if that character appears only once in the original string, or `)` if that character appears more than once in the original string. Ignore capitalization when determining if a character is a duplicate.

```js
const duplicateEncode = word => {
  // Your solution
}

console.log(duplicateEncode('din'));      // '((('
console.log(duplicateEncode('(( @'));     // '))(('
console.log(duplicateEncode('recede'));   // '()()()'
console.log(duplicateEncode('Success'));  // ')())())'
```

<details><summary>Solution</summary>

```js
const duplicateEncode = word => {
  word = word.toLowerCase();
  let result = '';
  for (let char of word) {
    word.indexOf(char) !== word.lastIndexOf(char)
    ? result += ')'
    : result += '(';
  }
  return result;
}
```

</details>

---

**[⬆ Back to Top](#javascript-coding-challenges-for-beginners)**

## 32. Reversed Strings

Write a function that reverses the string that is passed to it. For this challenge, you may __NOT__ use the JavaScript built-in `reverse()` method.

```js
const reverseString = str => {
  // Your solution
}

console.log(reverseString('hello'));  // 'olleh'
console.log(reverseString('world'));  // 'dlrow'
console.log(reverseString(''));       // ''
console.log(reverseString('h'));      // 'h'
```

<details><summary>Solution</summary>

```js
const reverseString = str => {
  let result = '';
  for (let char of str) {
    result = char + result;
  }
  return result;
}
```

</details>

---

**[⬆ Back to Top](#javascript-coding-challenges-for-beginners)**

## 33. Persistent Bugger

Write a function that takes a positive number `num` and returns its multiplicative persistence, which is the number of steps it takes to multiply all the digits of `num` by each other, and repeating with the product until a single digit is obtained.

```js
const persistence = num => {
  // Your solution
}

console.log(persistence(999));  // 4
// because 9*9*9=729, 7*2*9=126, 1*2*6=12, and finally 1*2=2

console.log(persistence(93));   // 3
// because 9*3=27, 2*7=14, 1*4=4 and 4 has only one digit

console.log(persistence(5));    // 0
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
}
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
}

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
}
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
  const map = new Map();

  for(let i = 0; i < nums.length; i++) {
    const otherIndex = map.get(target - nums[i]);
    if (typeof otherIndex !== 'undefined') {
      return [otherIndex, i];
    }
    map.set(nums[i], i);
  }
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

console.log(uniqueInOrder([1, 2, 2, 3, 3]));    // [1, 2, 3]
console.log(uniqueInOrder('ABBCcAD'));          // ['A', 'B', 'C', 'c', 'A', 'D']
console.log(uniqueInOrder('AAAABBBCCDAABBB'));  // ['A', 'B', 'C', 'D', 'A', 'B']
```

<details><summary>Solution</summary>

```js
const uniqueInOrder = iterable => {
  const len = iterable.length;
  let result = [];
  let lastItem;

  for (let i = 0; i < len; i++) {
    if (iterable[i] !== lastItem) {
      result.push(iterable[i]);
      lastItem = iterable[i];
    }
  }

  return result;
};
```

</details>

---

**[⬆ Back to Top](#javascript-coding-challenges-for-beginners)**

## 38. Best Time to Buy and Sell Stock

You are given an array `prices` where `prices[i]` is the price of a given stock on the `i`th day. You want to maximize your profit by choosing a single day to buy one stock and choosing a different day in the future to sell that stock. Return the maximum profit you can achieve from this transaction. If you cannot achieve any profit, return `0`.

Example 1:

```
Input: prices = [7,1,5,3,6,4]
Output: 5
Explanation: Buy on day 2 (price = 1) and sell on day 5 (price = 6), profit = 6-1 = 5.
Note that buying on day 2 and selling on day 1 is not allowed because you must buy before you sell.
```

Example 2:

```
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

Mike works as a DJ in the best London nightclub, and he often uses dubstep music in his performance. Recently, he has decided to take a couple of old songs and make dubstep remixes from them. Let's assume that a song consists of some number of words (that don't contain `WUB`). To make the dubstep remix of this song, Mike inserts a certain number of words `WUB` before the first word of the song (the number may be zero), after the last word (the number may be zero), and between words (at least one between any pair of neighbouring words), and then the boy glues together all the words, including `WUB`, in one string and plays the song at the club.

For example, a song with words "I AM X" can transform into a dubstep remix as `WUBWUBIWUBAMWUBWUBX` and cannot transform into `WUBWUBIAMWUBX`.

Recently, Johnny has heard Mike's new dubstep track, but since he isn't into modern music, he decided to find out what was the initial song that Mike remixed. Help Johnny restore the original song.

*Input*: The input consists of a single non-empty string, consisting only of uppercase English letters, the string's length doesn't exceed 200 characters

*Output*: Return the words of the initial song that Mike used to make a dubsteb remix. Separate the words with a space.

```js
const songDecoder = song => {
  // Your solution
}

console.log(songDecoder("AWUBBWUBC"));
// 'A B C' (WUB should be replaced by 1 space)
console.log(songDecoder("AWUBWUBWUBBWUBWUBWUBC"));
// 'A B C' (Multiples WUBs should be replaced by only 1 space)
console.log(songDecoder("WUBAWUBBWUBCWUB"));
// 'A B C' (Any starting or trailing WUBs should be removed)
console.log(songDecoder("WUBWEWUBAREWUBWUBTHEWUBCHAMPIONSWUBMYWUBFRIENDWUB"));
// 'WE ARE THE CHAMPIONS MY FRIEND'
```

<details><summary>Solution</summary>

```js
const songDecoder = song => {
  return song.replace(/(WUB)+/g, ' ').trim();
}
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
  let arr = Math.abs(x).toString().split('');
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

```
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

console.log(kidsWithCandies([2, 2, 1, 1, 2], 1)); // [true, false, false, false, false];
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

```
Input: accounts = [[1,5],[7,3],[3,5]]
Output: 10
Explanation: 
1st customer has wealth = 6
2nd customer has wealth = 10 
3rd customer has wealth = 8
The 2nd customer is the richest with a wealth of 10.
```

```js
const maximumWealth = accounts => {
   // Your solution
};

console.log(maximumWealth([[2,8,7],[7,1,3],[1,9,5]]));  // 17
console.log(maximumWealth([[1,5],[7,3],[3,5]]));        // 10
console.log(maximumWealth([[1,2,3],[3,2,1]]));          // 6
```

<details><summary>Solution</summary>

```js
const maximumWealth = accounts => {
  return Math.max(...accounts.map(customer => customer.reduce((a, b) => a + b)));
};
```

</details>

---

**[⬆ Back to Top](#javascript-coding-challenges-for-beginners)**
