# Software Engineering Interview Handbook (swe-interview-handbook)

Welcome to the Software Engineering Interview Handbook! This repository is a collection of resources, study guides, tips, and personal experiences aimed at helping both new and seasoned software engineers prepare for technical interviews.

## Table of Contents

1. [Introduction](#introduction)
2. [Getting Started](#getting-started)
3. [Topics Covered](#topics-covered)
   - [Big-O Notation](#big-o)
   - [Problem-Solving](#problem-solving)
   - [Data Structures](#data-structures)
     - [Arrays](#arrays)
4. [Study Guides](#study-guides)
5. [Interview Tips](#interview-tips)
6. [Practice Problems](#practice-problems)
7. [Mock Interviews](#mock-interviews)
8. [Contribution Guidelines](#contribution-guidelines)
9. [License](#license)

## Introduction

Hello and welcome! I am a budding software engineer, currently preparing for technical interviews and coding challenges. As I journey down this path, I found a wealth of information scattered across books, blog posts, online courses, and repositories. While I learned a lot from these sources, I noticed that there was no central, streamlined resource that catered to my specific learning style and pace.

This observation led me to start the Software Engineering Interview Handbook (swe-interview-handbook). The primary goal of this repository is to consolidate the knowledge, strategies, tips, and experiences that I gather during my preparation. I aim to structure this information in a way that's digestible and easy to review, not just for myself, but for anyone who may be embarking on a similar journey.

Through this repository, I hope to provide a comprehensive guide for software engineering interviews. From theoretical knowledge about data structures and algorithms to practical advice on how to present oneself in an interview, I intend to cover all aspects of the interview process.

Ultimately, my vision for this project is to create a community-driven platform where software engineers can share their insights and learn from one another, thereby elevating the entire field. I welcome and encourage contributions from all. Together, let's demystify the software engineering interview process.

## Getting Started

In this section, discuss the prerequisites for the repository (if any), how to navigate the repository, and how to use it effectively.

## Topics Covered

Here you can list down the topics covered in your study guides. The list might include Data Structures, Algorithms, Databases, System Design, Networking, etc.

## Big-O Notation

Big-O is the language used by programmers for measuring the efficiency of an algorithm. It helps answer if the optimizations made to an algorithm are helping or hurting.

Notes:

- Use logical variable names. Do not just use **n** everywhere.
- Constants are dropped: `O(2n) => O(n)`.
- Drop non-dominant terms: `O(n^2  + 3n + 2) => O(n^2)`.

## Problem-Solving

When given a question to solve, there are proven steps that I encourage you to follow before diving into coding:

1. **Verify the constraints**: Constraints are ways we can understand the question better so we know what kind of edge cases to consider as well as the different variables that might impact how you solve the question. This usually comes in the form of a dialog i.e. you want to ask your interviewer certain questions to answer and figure out what these constraints are.
   For example, for the famous `Two Sum` problem, you could ask:

   - Are all the numbers positive or can there be negatives? **Only positive.**
   - Are there duplicate numbers in the array? **No.**
   - Will there always be a solution available (i.e. given the array and the target, will we always be able to find two numbers that will add up to the target?) **No.**
   - What do we return if there's no solution? **Return null.**
   - Can multiple pairs add up to the target? **No.**
     Asking these questions demonstrates that you are thinking about all these edge cases and you're giving that onus on the actual person that gave you the task to figure out what the constraints are for the particular problem.

2. **Write out some test cases**: Test cases are just different combinations of the input we can receive. In the example of `Two Sum`, it would be different combinations of the array and the target we could get that would best capture all of these different edge cases that our solution wants to account for. This is a process you can work with your interviewer on where you ask them, "Is it okay if we come up with some test cases together that best capture these different questions that you've helped me answer for our constraints?".

```javascript
// The first test case we want to begin with is the Best Case Test Case. This is the text case that we know for sure what the answer will be for the given inputs we receive.
// arr = [1, 3, 7, 9, 2], t = 11, res = [3, 4]
// arr = [1, 3, 7, 9, 2], t = 25, res = null
// arr = [], t = 1, res = null
// arr = [5], t = 5, res = null
// arr = [1, 6], t = 7, res = [0, 1]
```

3. **Figure out a solution without code**: This is a very crucial step because what we're doing here is coming up with a working solution before we get bogged down by any technical details. Don't think about the code implementation. Just think of a working logical solution for how you might solve this problem if you were just asked the question out of the blue. So, if there's no code involved, you don't want to think about for loop, while loop, variables, etc. All you want to think about is if I were to approach this problem critically and logically, how would I ensure that I have a working solution for all the test cases that I came up with?

Start with the best-case test case that you came up with. In this step, don't think about optimal solutions, we just want to make sure that we have a working solution because a working solution is way better than a non-working optimal solution.

4. **Write out your solution in code**: Convert your algorithm to code.

5. **Double-check for errors**: Make sure that you did not make any spelling mistakes or typos. Variable names should be consistent wherever they are used. All of your cases should be correct. All your loops and functions should be properly closed. The main key here is that you want to do the due diligence check to make sure that your code is exactly how it should be for it to work properly. Essentially, you should be able to copy this into an IDE and the code should work perfectly. Your interviewer is looking for these mistakes and trying to see if you're a careful coder.

6. **Test your code with your test cases**: At this step, what we're doing is testing the solution we wrote against our test case. This is a crucial step because the interviewer is going to make you do exactly this. They want to make sure that you understand what every step of the code you wrote is doing. The only way for them to verify that is by asking you to walk through the solution using one of your test cases. So they want you to keep track of all the variables you're setting and how the code is going to flow and your logic. So, this is important to practice because without practice you might stumble upon having to walk through your code rigorously.

7. **Analyze space and time complexity**: When you're analyzing space and time complexity, you're trying to identify the relative relationship of how much of the time and space resources your code will consume based on the size of your inputs. Meaning that if you have inputs that scale, which they generally always will, in our particular case, how much more time and space resources is your code going to take?

With time complexity, you're thinking about how many more iterations your code has to run if the array gets bigger.

8. **Can you optimize your solution?**: When you compare space and time complexities, if one of them is drastically better than the other, that is a good hint that maybe you can consume more resources in the complexity that is much better to bring down the other complexity.

## Data Structures

### - Arrays

Arrays hold elements of the same data type in contiguous blocks of memory and are indexed by contiguous integers. Different programming languages implement arrays differently under the hood. For instance, in languages like C, arrays have a fixed size that you need to define beforehand. Whereas in languages like Python, arrays (or lists in Python) are dynamic. These differences can affect the time complexity of operations made to the array.

### Advantages

- Constant time access to read and write array elements
- Store multiple elements

### Disadvantages

- Adding and removing elements from the start or middle is an O(n) operation (i.e. linear time operation). However, doing so from the end is an O(1) (i.e. constant operation) operation.

### Key Takeaways

- The ith element of a one-dimensional array is accessed using `arr[i]` and the index math is `(addr of arr) + ((size of an element in the arr) * (i - first_index of arr))`.
- The (r, c) element of a two-dimensional array (referred to as matrix) is accessed using `arr[i][j]` and the index math is `(r - first_row_index) * (size of row) + (c - first_column_index)`.
- If rows are sequentially completed first during accessing elements in a two-dimensional array, it is called row-major access. It is called column-major access for columns.

## Study Guides

In this section, provide links to the various study guides you have created, ideally organized by topic.

## Interview Tips

Provide tips and tricks you've gathered from your own experience and research to help others perform better in interviews.

## Practice Problems

Share practice problems or links to problem sets that you've found particularly useful in your own studies.

## Mock Interviews

If you plan to include anything related to mock interviews or want to share your experience, you can discuss that in this section.

## Contribution Guidelines

If you are open to contributions, provide instructions on how others can contribute to this repository. It's a good idea to also include a code of conduct for contributors.

## License

Include the license for your project, usually added at the bottom of the README. This is important if you want others to use or contribute to your project.
