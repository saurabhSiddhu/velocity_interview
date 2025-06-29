# Day 1 Mock Interview Solutions: Aptitude & C MCQs

**Date:** 2025-06-28

---

## Section 1: Aptitude Solutions

1. **Time & Work:**
   - 4 men can complete a work in 6 days, so total work = 4 × 6 = 24 man-days. If 3 men are assigned, days required = 24 / 3 = **8 days**.
   - **Explanation:** The total amount of work is measured in man-days. If fewer men are available, the work takes proportionally more days. Formula: Men × Days = Work.
2. **Profit & Loss:**
   - Cost Price (CP) = $200, Selling Price (SP) = $250. Profit = SP - CP = $50. Profit % = (Profit / CP) × 100 = (50/200) × 100 = **25%**.
   - **Explanation:** Profit percentage is always calculated on the cost price. Subtract CP from SP to get profit, then divide by CP and multiply by 100.
3. **Speed & Distance:**
   - Distance = 60 km, Time = 1.5 hours. Speed = Distance / Time = 60 / 1.5 = **40 km/h**.
   - **Explanation:** Speed is the ratio of distance covered to time taken. Always ensure units are consistent.
4. **Percentages:**
   - 20% of 150 = (20/100) × 150 = **30**.
   - **Explanation:** To find x% of y, multiply y by x/100. This gives the part of the whole represented by the percentage.
5. **Averages:**
   - Numbers: 5, 7, 9, 11, 13. Average = (5 + 7 + 9 + 11 + 13) / 5 = 45 / 5 = **9**.
   - **Explanation:** The average is the sum of all values divided by the number of values.
6. **Ratio & Proportion:**
   - Ratio of boys to girls = 3:2, total students = 30. Total parts = 3 + 2 = 5. Each part = 30 / 5 = 6. Number of girls = 2 × 6 = **12**.
   - **Explanation:** Divide the total by the sum of ratio parts to get the value of one part, then multiply by the required part.
7. **Simple Interest:**
   - Principal (P) = $1000, Rate (R) = 5%, Time (T) = 2 years. SI = (P × R × T) / 100 = (1000 × 5 × 2) / 100 = **$100**.
   - **Explanation:** Simple interest is calculated on the original principal for the entire period.
8. **Compound Interest:**
   - Principal = $2000, Rate = 10%, Time = 2 years. CI = 2000 × (1 + 0.10)^2 - 2000 = 2000 × 1.21 - 2000 = 2420 - 2000 = **$420**.
   - **Explanation:** Compound interest is calculated on the new principal each year. Use the formula: CI = P × (1 + R/100)^T - P.
9. **Ages:**
   - Let son's age = x, father's age = 60 - x. After 5 years: (60 - x) + 5 = 2(x + 5). So, 65 - x = 2x + 10 → 65 - 10 = 2x + x → 55 = 3x → x = 18⅓ (son), father = 41⅔.
   - **Explanation:** Set up equations based on the information, then solve for the unknowns step by step.
10. **Logical Reasoning:**
    - The statement says some flowers fade quickly and all roses are flowers. It does not guarantee that any rose is among the flowers that fade quickly. So, the answer is No.
    - **Explanation:** Logical deduction requires that the subset relationship is explicit. Here, roses may or may not be among the flowers that fade quickly.

---

## Section 2: C Language MCQs Solutions

1. **Output:**
   - 5 / 2 = **2** (Option B). Integer division in C truncates the decimal part.
   - **Explanation:** In C, dividing two integers results in an integer. The fractional part is discarded, not rounded.
2. **Output:**
   - arr[3] is out of bounds. Likely prints **garbage value** (Option C), undefined behavior.
   - **Explanation:** Accessing an array index outside its bounds in C leads to undefined behavior. It may print a garbage value or cause a crash.
3. **Error:**
   - Assignment used instead of comparison (Option B). Should be if(x == 5).
   - **Explanation:** '=' is the assignment operator, '==' is the comparison operator. Using '=' in a condition assigns the value and always evaluates to true (if nonzero).
4. **Output:**
   - Only printf is inside the loop, i++ is outside. Infinite loop printing 0 (Option C).
   - **Explanation:** The increment statement is outside the loop, so the loop variable never changes, causing an infinite loop.
5. **Output:**
   - sizeof('A') is usually 4 (Option C), as 'A' is int in C.
   - **Explanation:** In C, character constants like 'A' are of type int, not char. On most systems, sizeof(int) is 4 bytes.
6. **Output:**
   - ++a + a++ is undefined behavior, but often results in 22 (Option B) on many compilers.
   - **Explanation:** Modifying a variable more than once between sequence points leads to undefined behavior. The result may vary, but often gives 22 if a starts at 10.
7. **Error:**
   - arr[2] = 3; is out of bounds for int arr[2]; (Option B).
   - **Explanation:** Declaring int arr[2] creates an array with indices 0 and 1. arr[2] is out of bounds and may cause undefined behavior.
8. **Output:**
   - x == 5 ? 10 : 20 evaluates to 10 (Option B).
   - **Explanation:** The ternary operator returns the first value if the condition is true, otherwise the second. Here, x == 5 is true.
9. **Output:**
   - Prints 0 1 2 (Option A). for(; i < 3;) printf("%d ", i++);
   - **Explanation:** The loop starts with i = 0 and increments after printing. It prints 0, 1, 2 and then exits.
10. **Error:**
    - int *p; *p = 10; dereferences uninitialized pointer (Option B).
    - **Explanation:** Declaring a pointer without initialization and then dereferencing it leads to undefined behavior, possibly a crash.

---

**End of Day 1 Solutions**
