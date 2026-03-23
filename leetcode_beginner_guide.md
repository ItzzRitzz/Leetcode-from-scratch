# LeetCode Beginner's Guide: How to Use the Platform
## Everything You Need to Know to Get Started

---

## PART 1: Setting Up Your LeetCode Account

### Step 1: Create Account
1. Go to **leetcode.com**
2. Click **Sign Up**
3. Choose: Email or Google login (Google is faster)
4. Verify email
5. Done! ✅

### Step 2: Choose Python 3 as Default Language
1. After login, go to **Settings** (top right → gear icon)
2. Find **Default Language**
3. Select **Python 3**
4. Save ✅

### Step 3: Bookmark These Pages
- **Easy Problems**: https://leetcode.com/problemset/all/?difficulty=EASY
- **Your Submissions**: https://leetcode.com/submissions/
- **Discuss Section**: https://leetcode.com/discuss/

---

## PART 2: Understanding the Problem Interface

### Problem Page Layout

```
┌─────────────────────────────────────────────────┐
│ Problem Title (e.g., "Two Sum")                │
├─────────────────────────────────────────────────┤
│ LEFT SIDE                 │  RIGHT SIDE         │
│                           │                     │
│ • Description            │ • Code Editor       │
│ • Constraints            │ • Run Test Cases    │
│ • Examples               │ • Submit            │
│ • Solutions (after solve)│ • Reset             │
│                           │                     │
└─────────────────────────────────────────────────┘
```

### What Each Section Means

**LEFT SIDE - Problem Description:**

```
DESCRIPTION
├─ Problem Statement
│  (What you need to do - READ THIS CAREFULLY!)
│
├─ Constraints  
│  (Limits on input size - read after understanding problem)
│
├─ Examples
│  (Test cases - very important! Use these to verify)
│
└─ Follow Up
   (Optional harder version - ignore for now)
```

**RIGHT SIDE - Code Editor:**
- Where you write Python code
- Has template function ready
- You fill in the function body

---

## PART 3: Step-by-Step Solving a Problem

### Let's Solve Your First Problem: "Two Sum"

### STEP 1: Navigate to Two Sum
1. Go to **Easy Problems** filter
2. Search for "Two Sum" (first problem usually)
3. Click on it

### STEP 2: READ THE PROBLEM (VERY CAREFULLY!)

```
Title: Two Sum

Description:
Given an array of integers nums and an integer target, 
return the indices of the two numbers such that they add up to target.

You may assume that each input has exactly one solution, 
and you may not use the same element twice.

You can return the answer in any order.

Example 1:
Input: nums = [2,7,11,15], target = 9
Output: [0,1]
Explanation: nums[0] + nums[1] == 9, so we return [0, 1].

Example 2:
Input: nums = [3,2,4], target = 6
Output: [1,2]

Example 3:
Input: nums = [3,3,6], target = 6
Output: [0,1]

Constraints:
2 <= nums.length <= 10^4
-10^9 <= nums[i] <= 10^9
-10^9 <= target <= 10^9
Only one valid answer exists.
```

### STEP 3: UNDERSTAND THE PROBLEM
Ask yourself:
- ✅ What am I given? (array + target number)
- ✅ What do I return? (indices, not values!)
- ✅ What are the constraints? (use any pair once, exactly one solution)
- ✅ Do I understand all examples?

### STEP 4: THINK (NOT CODE!)
Don't open the code editor yet!

**Plan your approach:**
```
Approach 1 (Brute Force):
- Try every pair of numbers
- Check if they add to target
- If yes, return indices

Time Complexity: O(n²)  [slow but okay for learning]

Approach 2 (Efficient):
- Use dictionary to remember numbers
- As you go through list:
  - Calculate: complement = target - current_number
  - Check if complement exists in dictionary
  - If yes, return both indices
  - If no, add current_number to dictionary

Time Complexity: O(n)  [better, but harder]
```

### STEP 5: CODE YOUR SOLUTION

Open the code editor. You'll see:

```python
class Solution:
    def twoSum(self, nums: List[int], target: int) -> List[int]:
        # Write your code here
        
        pass  # Remove this line
```

**Replace with:**

```python
class Solution:
    def twoSum(self, nums: List[int], target: int) -> List[int]:
        # Dictionary to store numbers we've seen
        seen = {}
        
        # Go through each number with index
        for i in range(len(nums)):
            # What number do we need?
            complement = target - nums[i]
            
            # Have we seen this number before?
            if complement in seen:
                # Found the pair!
                return [seen[complement], i]
            
            # Remember this number
            seen[nums[i]] = i
        
        # No pair found (shouldn't happen per constraints)
        return []
```

### STEP 6: TEST WITH EXAMPLES

Click **"Run"** button

Enter test case:
```
nums = [2,7,11,15]
target = 9
```

**Expected Output:** [0,1]

**Your Output:** Should also show [0,1] ✅

Try other examples:
- nums = [3,2,4], target = 6 → [1,2]
- nums = [3,3,6], target = 6 → [0,1]

### STEP 7: SUBMIT

Once tests pass, click **"Submit"**

You'll see:
- **Accepted** ✅ (You solved it!)
- **Wrong Answer** ❌ (Debug and retry)
- **Time Limit Exceeded** (Solution too slow, rare for easy)

---

## PART 4: What to Do After Solving

### If You Got "Accepted" ✅

1. **Celebrate!** 🎉
2. **Review your solution** (make sure you understand it)
3. **Check the "Discuss" tab** for other approaches
4. **Note any new patterns** you learned
5. **Move to next problem**

### If You Got "Wrong Answer" ❌

1. **Don't panic** - this is normal!
2. **Re-read the problem** - you missed something
3. **Test your code manually** with the examples
4. **Add print statements** to debug:

```python
def twoSum(self, nums, target):
    seen = {}
    
    for i in range(len(nums)):
        complement = target - nums[i]
        print(f"i={i}, nums[i]={nums[i]}, complement={complement}")  # Debug
        
        if complement in seen:
            return [seen[complement], i]
        
        seen[nums[i]] = i
    
    return []
```

4. **Understand what went wrong**
5. **Fix and try again**

---

## PART 5: How to Read Discuss/Solutions

### After solving, look at other solutions:

1. Click **Solutions** tab at bottom
2. See official explanation
3. Click **Discuss** for user solutions

### What to Look For:
- ✅ **Correct approaches** (multiple ways to solve)
- ✅ **Time/Space complexity** explanation
- ❌ **Don't memorize** - understand the logic
- ❌ **Don't copy-paste** to other problems

### Example from Discuss:

```python
# Approach 1: Using Dictionary (Recommended for beginners)
class Solution:
    def twoSum(self, nums: List[int], target: int) -> List[int]:
        """
        Time Complexity: O(n)   [linear, very fast]
        Space Complexity: O(n)  [need dictionary]
        """
        seen = {}
        for i, num in enumerate(nums):
            if target - num in seen:
                return [seen[target - num], i]
            seen[num] = i


# Approach 2: Brute Force (Simple but slow)
class Solution:
    def twoSum(self, nums: List[int], target: int) -> List[int]:
        """
        Time Complexity: O(n²)  [slow for large inputs]
        """
        for i in range(len(nums)):
            for j in range(i + 1, len(nums)):
                if nums[i] + nums[j] == target:
                    return [i, j]
```

---

## PART 6: LeetCode Tips & Tricks

### Tip 1: Filter by Difficulty
```
Problem Set → Filter → Difficulty (Easy)
Start with Easy: 800+ problems
```

### Tip 2: Use "List of Problems"
1. Go to **Explore**
2. Select **LeetCode 75** or **LeetCode 150** (curated lists)
3. Start from beginning

### Tip 3: Track Your Progress
- LeetCode shows solved problems with ✅
- Shows your submission history
- Shows your best solution

### Tip 4: Favorite Problems
- Click ⭐ on useful problems
- Easily review later

### Tip 5: Use Tags
- Filter by topic (Array, String, Hash Table)
- Learn one pattern at a time

---

## PART 7: Common LeetCode Terminology

| Term | Meaning |
|------|---------|
| **Accepted** | Your solution is correct ✅ |
| **Wrong Answer** | Output doesn't match expected ❌ |
| **Time Limit Exceeded** | Your code is too slow |
| **Runtime Error** | Your code crashed |
| **Compile Error** | Syntax error in code |
| **Test Case** | Sample input/output to verify |
| **Edge Case** | Special/extreme inputs |
| **Submission** | When you click Submit |

---

## PART 8: Your First Week on LeetCode

### Day 1:
```
Problem: Running Sum of 1d Array
Difficulty: Easy
Time: 30-45 mins
Goal: Get comfortable with interface
```

### Day 2:
```
Problem: Richest Customer Wealth
Difficulty: Easy
Time: 30-45 mins
Goal: Solve without looking at hints
```

### Day 3:
```
Problem: Two Sum
Difficulty: Easy
Time: 45-60 mins
Goal: Use hash map technique
```

### Day 4:
```
Problem: Palindrome Number
Difficulty: Easy
Time: 20-30 mins
Goal: Quick solve
```

### Day 5:
```
Problem: Contains Duplicate
Difficulty: Easy
Time: 20-30 mins
Goal: Use sets
```

### Day 6:
```
Review all 5 problems
Time: 30-45 mins
Goal: Understand patterns
```

### Day 7:
```
Pick 2 new easy problems
Time: 60 mins
Goal: Practice independently
```

---

## PART 9: Debugging Your Code

### When Code Doesn't Work:

**Step 1: Check Syntax**
```python
# ❌ Wrong
def solve(nums):
    for i in range(nums)
        print(i)

# ✅ Correct
def solve(nums):
    for i in range(len(nums)):
        print(i)
```

**Step 2: Test with Examples**
```python
# Add print statements
def twoSum(nums, target):
    seen = {}
    
    for i in range(len(nums)):
        complement = target - nums[i]
        print(f"Checking index {i}: {nums[i]}, need {complement}")
        
        if complement in seen:
            return [seen[complement], i]
        
        seen[nums[i]] = i
    
    return []

# Call with example
result = twoSum([2, 7, 11, 15], 9)
print(f"Result: {result}")  # Should be [0, 1]
```

**Step 3: Check Edge Cases**
```python
# Empty array?
# Single element?
# Negative numbers?
# Duplicates?
```

---

## PART 10: Common Beginner Mistakes

### Mistake 1: Not Reading Carefully
```
❌ Problem: Find two numbers that sum to target
You did: Return the numbers themselves
Should: Return their INDICES
```
**Fix:** Read problem 3 times before coding

### Mistake 2: Not Testing Manually
```
❌ Submit without testing
Should: Test with ALL examples first
```

### Mistake 3: Wrong Variable Names
```python
❌ def twoSum(nums, target):
    return nums  # Wrong!

✅ def twoSum(nums, target):
    # ... proper code ...
    return [index1, index2]  # Correct!
```

### Mistake 4: Forgetting About Edge Cases
```python
❌ Code works for [2,7,11,15] but fails for [2,2,11,15]
Should: Test with duplicates, negatives, etc.
```

### Mistake 5: Off-by-One Errors
```python
❌ for i in range(len(nums)-1):  # Misses last element!
✅ for i in range(len(nums)):    # Correct
```

---

## PART 11: When You Get Stuck (Decision Tree)

```
               Stuck on Problem?
                      |
              Have you tried for
              30 minutes?
                |         |
               No        Yes
               |         |
            Keep      ┌──┴──┐
            trying   A     B
                    Can  Can't
                    you  understand
                    understand? how
                       |      |
                    Yes    No
                    |       |
                  Great!   Look at
                  Move     Solutions
                  on       ↓
                         Read & Understand
                         ↓
                         Try Again
                         ↓
                         Move On
```

---

## PART 12: Your Success Checklist

**For each problem, make sure:**
- [ ] Read problem carefully (2+ times)
- [ ] Understood all examples
- [ ] Thought of approach before coding
- [ ] Wrote code in editor
- [ ] Tested with ALL examples
- [ ] Code passed all tests
- [ ] Understood the solution
- [ ] Noted any new patterns
- [ ] Could explain it to someone else

---

## FINAL ADVICE

```
Week 1: Focus on solving
Week 2: Focus on understanding
Week 3: Focus on patterns
Week 4+: Focus on consistency

Remember:
✅ Slow and steady wins the race
✅ Understanding > Memorizing
✅ Consistency > Speed
✅ You will struggle - that's normal
✅ After 20 problems, you'll see patterns
✅ After 50 problems, you'll think differently
```

---

**You're ready! Go solve your first problem! 🚀**

Need help? Check:
1. This guide
2. Python guide
3. Your study plan
4. LeetCode Discuss section
