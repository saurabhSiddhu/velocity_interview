# Day 1 Mock Interview Solutions: JavaScript and Essay

**Date:** 2025-06-28

---

## Section 1: JavaScript Coding Solutions

1. **Reverse a string:**

```js
// Method 1: Using built-in reverse()
function reverseString(str) {
  // Convert the string to an array, reverse, and join back
  return str.split("").reverse().join("");
}
// Example: reverseString('hello') => 'olleh'

// Method 2: Using a for loop (no reverse method)
function reverseStringLoop(str) {
  let reversed = "";
  for (let i = str.length - 1; i >= 0; i--) {
    reversed += str[i];
  }
  return reversed;
}
// Example: reverseStringLoop('hello') => 'olleh'

// Method 3: Using a while loop (no reverse, no array methods, no repeat)
function reverseStringWhileNoRepeat(str) {
  let reversed = "";
  let i = str.length - 1;
  while (i >= 0) {
    reversed += str[i];
    i--;
  }
  return reversed;
}
// Example: reverseStringWhileNoRepeat('hello') => 'olleh'

// Method 4: Using recursion (no reverse, no array methods, no repeat)
function reverseStringRecursiveNoRepeat(str) {
  if (str === "") return "";
  return reverseStringRecursiveNoRepeat(str.substr(1)) + str[0];
}
// Example: reverseStringRecursiveNoRepeat('hello') => 'olleh'
```

**Detailed Explanation:**

- **Method 1:**
  - `split("")` converts the string into an array of characters.
  - `reverse()` reverses the array in place.
  - `join("")` joins the reversed array back into a string.
  - This is the most concise and idiomatic way in JavaScript, but uses the built-in reverse method.
- **Method 2:**
  - Initializes an empty string `reversed`.
  - Loops from the last character to the first (i = str.length - 1 to 0).
  - Appends each character to `reversed`.
  - Returns the reversed string. This method does not use `reverse()` and is efficient for interviews.
- **Method 3:**
  - Initializes an empty string `reversed` and an index `i` at the last character.
  - While `i` is greater than or equal to 0, appends `str[i]` to the `reversed` and decrements `i`.
  - Returns the reversed string. This method uses a `while` loop, no array methods, and does not use `repeat()`.
- **Method 4:**
  - Uses recursion to reverse the string.
  - Base case: if the string is empty, return an empty string.
  - Recursive case: call the function on the substring from index 1, then add the first character to the end. This method does not use array methods and does not use `repeat()`.
- All methods achieve the same result. Methods 2, 3, and 4 do not use the built-in reverse() function, array methods, or `repeat()`.
- **Step-by-step (Method 3):**
  1. Start with an empty string and index at the last character.
  2. While index >= 0, append str[i] to the result and decrement i.
  3. Return the reversed string.
- **Step-by-step (Method 4):**
  1. Base case: if the string is empty, return empty string.
  2. Recursive case: call the function on the substring from index 1, then add the first character to the end.

2. **Sum of array elements:**

```js
function sumArray(arr) {
  // Use reduce to accumulate the sum of all elements in the array
  // The callback takes the running sum and the current number
  return arr.reduce((sum, num) => sum + num, 0);
}
// Example: sumArray([1,2,3]) => 6
```

**Detailed Explanation:**

- The `reduce()` method iterates through the array, applying the function `(sum, num) => sum + num` to each element.
- `sum` starts at 0 (the second argument to reduce).
- For each element, `num` is added to `sum`.
- The final result is the sum of all elements in the array.
- This is concise, efficient, and the standard way to sum arrays in JavaScript.
- **Step-by-step:**
  1. sum = 0, num = 1 → sum = 1
  2. sum = 1, num = 2 → sum = 3
  3. sum = 3, num = 3 → sum = 6

3. **Pattern printing (n = 3):**

```js
// Method 1: Using repeat()
function printPattern(n) {
  // Loop from 1 to n, printing a line with i asterisks each time
  for (let i = 1; i <= n; i++) {
    console.log("*".repeat(i));
  }
}
// Output:
// *
// **
// ***

// Method 2: Without using repeat()
function printPatternNoRepeat(n) {
  for (let i = 1; i <= n; i++) {
    let line = "";
    for (let j = 0; j < i; j++) {
      line += "*";
    }
    console.log(line);
  }
}
// Output:
// *
// **
// ***
```

**Detailed Explanation:**

- **Method 1:**
  - Uses `repeat()` to create a string of `i` asterisks for each line.
  - Simple and concise, but relies on the built-in repeat function.
- **Method 2:**
  - Uses a nested loop: the outer loop controls the number of lines, the inner loop builds a string of asterisks by concatenation.
  - Does not use `repeat()` or any advanced string methods.
  - This approach is useful in interviews where use of built-in methods is restricted.
- Both methods produce the same output: a left-aligned triangle of asterisks.
- **Step-by-step (Method 2):**
  1. For each line from 1 to n, start with an empty string.
  2. Add one asterisk at a time until the line has the required number.
  3. Print the line.

4. **Check if a string is a palindrome:**

```js
function isPalindrome(str) {
  // Compare the string to its reverse (case-sensitive, no cleaning)
  return str === str.split("").reverse().join("");
}
// Example: isPalindrome('madam') => true
// Example: isPalindrome('hello') => false
```

**Detailed Explanation:**

- The function checks if the input string reads the same forwards and backwards.
- `str.split("").reverse().join("")` creates the reversed version of the string.
- The function returns true if the original string and the reversed string are identical (case-sensitive, includes all characters).
- No cleaning or case conversion is performed, so 'Madam' and 'madam' are not considered equal.
- **Step-by-step:**
  1. Input: 'madam' → Reverse: 'madam' → true
  2. Input: 'hello' → Reverse: 'olleh' → false

5. **Find the first non-repeating character in a string:**

```js
function firstNonRepeatingChar(str) {
  // Create a frequency map
  const freq = {};
  for (let char of str) {
    freq[char] = (freq[char] || 0) + 1;
  }
  // Find the first character with frequency 1
  for (let i = 0; i < str.length; i++) {
    if (freq[str[i]] === 1) return str[i];
  }
  return null;
}
// Example: firstNonRepeatingChar('aabbcde') => 'c'
```

**Detailed Explanation:**

- The function finds the first character in the string that does not repeat.
- First, it creates a frequency map (object) to count occurrences of each character.
- It then iterates through the string by index, checking if the frequency of each character is 1.
- The first such character is returned; if all characters repeat, the function returns null.
- This approach ensures the first unique character is found, including the first character if it is unique.
- **Step-by-step:**
  1. Input: 'aabbcde'
  2. Frequency map: {a:2, b:2, c:1, d:1, e:1}
  3. First non-repeating: 'c'

---

## Section 2: Essay Sample

**The impact of technology in daily life**

Technology has revolutionized every aspect of our daily lives. From the way we communicate to how we work, shop, and learn, technology has made processes faster, easier, and more efficient. Smartphones and the internet have connected people globally, enabling instant communication and access to information. Online banking, e-commerce, and digital payments have simplified financial transactions. In education, e-learning platforms provide flexible learning opportunities. However, over-reliance on technology can lead to reduced face-to-face interactions and privacy concerns. Overall, technology continues to shape our world, offering immense benefits while also presenting new challenges that society must address.

**Explanation:**

- The essay introduces the topic, discusses several areas of impact (communication, work, education, finance), and mentions both benefits and drawbacks.
- It is structured with an introduction, body, and conclusion, as expected in a short essay.
- The content is relevant, concise, and covers multiple perspectives on technology's influence.

---

**End of Day 1 Solutions**
