![javascript](images/logo-js.png)

# [Codewars](https://www.codewars.com/) JavaScript Solutions

## Challenges

|  Kyu  | Questions                                   |
| :---: | :------------------------------------------ |
|   8   | [Even or Odd](#even-or-odd)                 |
|   8   | [Keep Hydrated!](#keep-hydrated)                 |
|   6   | [Multiples of 3 or 5](#multiples-of-3-or-5) |
|   7   | [Vowel Count](#vowel-count)                 |

---

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

console.log(even_or_odd(0));  // 'Even'
console.log(even_or_odd(2));  // 'Even'
console.log(even_or_odd(3));  // 'Odd'
console.log(even_or_odd(-3)); // 'Odd'
```

</details>

---

**[⬆ Back to Top](#challenges)**

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

console.log(litres(0)); // 0
console.log(litres(2)); // 1
console.log(litres(1.4)); // 0
console.log(litres(12.3)); // 6
console.log(litres(0.82)); // 0
console.log(litres(11.8)); // 5
console.log(litres(1787)); // 893
```

</details>

---

**[⬆ Back to Top](#challenges)**

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

console.log(solution(0));   // 0
console.log(solution(-15)); // 0
console.log(solution(10));  // 23
console.log(solution(20));  // 78
console.log(solution(200)); // 9168
```
</details>

---

**[⬆ Back to Top](#challenges)**

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

console.log(getCount('my pyx')); // 0
console.log(getCount('pear tree')); // 4
console.log(getCount('abracadabra')); // 5
console.log(getCount('o a kak ushakov lil vo kashu kakao')); // 13
```

</details>

---

**[⬆ Back to Top](#challenges)**
