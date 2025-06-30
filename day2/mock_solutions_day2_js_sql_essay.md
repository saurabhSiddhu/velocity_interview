# Day 2: Solutions (JavaScript Coding, SQL, and Essay)

## JavaScript Coding Solutions

### 1. Reverse a String (Unicode, spaces, no built-in reverse)

**Iterative:**

```js
function reverseStringIterative(str) {
  let rev = "";
  for (let i = str.length - 1; i >= 0; i--) {
    rev += str[i];
  }
  return rev;
}
```

**Recursive:**

```js
function reverseStringRecursive(str) {
  if (str === "") return "";
  return reverseStringRecursive(str.substr(1)) + str[0];
}
```

### 2. Find the Kth Largest Element in Array (No sort)

```js
function kthLargest(arr, k) {
  let copy = arr.slice();
  for (let i = 0; i < k; i++) {
    let max = -Infinity,
      idx = -1;
    for (let j = 0; j < copy.length; j++) {
      if (copy[j] > max) {
        max = copy[j];
        idx = j;
      }
    }
    copy[idx] = -Infinity;
    if (i === k - 1) return max;
  }
}
```

### 3. Check for Anagram (case-insensitive, ignore spaces)

**Iterative:**

```js
function isAnagramIterative(str1, str2) {
  str1 = str1.replace(/\s/g, "").toLowerCase();
  str2 = str2.replace(/\s/g, "").toLowerCase();
  if (str1.length !== str2.length) return false;
  let count = {};
  for (let ch of str1) count[ch] = (count[ch] || 0) + 1;
  for (let ch of str2) {
    if (!count[ch]) return false;
    count[ch]--;
  }
  return true;
}
```

**Recursive:**

```js
function isAnagramRecursive(str1, str2) {
  str1 = str1.replace(/\s/g, "").toLowerCase();
  str2 = str2.replace(/\s/g, "").toLowerCase();
  if (str1.length !== str2.length) return false;
  if (str1.length === 0) return true;
  let idx = str2.indexOf(str1[0]);
  if (idx === -1) return false;
  return isAnagramRecursive(
    str1.slice(1),
    str2.slice(0, idx) + str2.slice(idx + 1)
  );
}
```

### 4. Print Number Pyramid Pattern

**Iterative:**

```js
function printPyramidIterative(n) {
  for (let i = 1; i <= n; i++) {
    let line = " ".repeat(n - i);
    for (let j = 1; j <= i; j++) {
      line += j + " ";
    }
    console.log(line.trimEnd());
  }
}
```

**Recursive:**

```js
function printPyramidRecursive(n, i = 1) {
  if (i > n) return;
  let line = " ".repeat(n - i);
  for (let j = 1; j <= i; j++) {
    line += j + " ";
  }
  console.log(line.trimEnd());
  printPyramidRecursive(n, i + 1);
}
```

### 5. Sum of Digits Until Single Digit (Recursion)

```js
function digitalRoot(n) {
  if (n < 10) return n;
  let sum = 0;
  while (n > 0) {
    sum += n % 10;
    n = Math.floor(n / 10);
  }
  return digitalRoot(sum);
}
```

---

## Essay/Article Sample

**Remote Work vs. Office Work: Pros, Cons, and the Future of Work**

_Introduction:_
The debate between remote work and office work has intensified in recent years, especially after the global shift caused by the pandemic. Both models offer unique advantages and challenges, shaping the future of work.

_Body:_
Remote work provides flexibility, allowing employees to balance personal and professional lives more effectively. It reduces commuting time and costs, and can boost productivity for self-motivated individuals. However, it may lead to feelings of isolation, communication gaps, and difficulty in separating work from home life. Office work, on the other hand, fosters collaboration, team spirit, and easier access to resources. It enables spontaneous discussions and a clear boundary between work and personal time, but can be rigid and time-consuming due to daily commutes. The future likely lies in a hybrid model, combining the best of both worlds, with technology enabling seamless collaboration regardless of location.

_Conclusion:_
Both remote and office work have their merits and drawbacks. Organizations should focus on flexibility, employee well-being, and leveraging technology to create productive and inclusive work environments for the future.

---

**Review & Self-Assessment:**

- Check your code for clarity and correctness.
- Practice explaining your logic out loud.
- Review the essay for structure and key points.
- Focus on areas where you struggled and plan to improve tomorrow.
