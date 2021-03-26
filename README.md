![javascript](images/logo-js.png)

# JavaScript Coding Challenges for Beginners

## Multiples of 3 or 5

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

## Even or Odd

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

## Clock

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

## Returning Strings

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

## Century From Year

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

## Keep Hydrated!

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

## Is n Divisible by x and y?

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

## Vowel Count

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

## Disemvowel Trolls

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

## Find the Odd Int

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

## Get the Middle Character

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

## Who likes it?

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

## Create Phone Number

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

## Square Every Digit

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

## You're a square!

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

## Highest and Lowest

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

## Descending Order

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

## Mumbling

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
