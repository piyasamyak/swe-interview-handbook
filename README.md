# Software Engineering Interview Handbook (swe-interview-handbook)

Welcome to the Software Engineering Interview Handbook! This repository is a collection of resources, study guides, tips, and personal experiences aimed at helping both new and seasoned software engineers prepare for technical interviews.

## Table of Contents

1. [Introduction](#introduction)
2. [Getting Started](#getting-started)
3. [Topics Covered](#topics-covered)
   - [Big-O Notation](#big-o)
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

### Big-O Notation

Big-O is the language used by programmers for measuring the efficiency of an algorithm. It helps answer if the optimizations made to an algorithm is helping or hurting.

Notes:

- Use logical variable names. Do not just use **n** everywhere.
- Constants are dropped: `O(2n) => O(n)`.
- Drop non-dominant terms: `O(n^2  + 3n + 2) => O(n^2)`.

### Data Structures

#### Arrays

Arrays hold elements of the same data type in contiguous blocks of memory and indexed by contiguous integers. Different programming languages implement arrays differently under the hood. For instance, in languages like C, arrays have a fixed size that you need to define beforehand. Whereas in languages like Python, arrays (or list in Python) are dynamic. These differences can affect the time complexity of operations made to the array.

##### Advantages

- Constant time access to read and write array elements
- Store multiple elements

#### Disadvantages

- Adding and removing elements from the start or middle is an O(n) operation (i.e. linear time operation). However, doing so from the end is an O(1) (i.e. constant operation) operation.

#### Key Takeaways

- The ith element of a one dimensional array is accessed using `arr[i]` and the index math is `(addr of arr) + ((size of an element in the arr) * (i - first_index of arr))`.
- The (r, c) element of a two dimensional array (referred to as matrix) is accessed using `arr[i][j]` and the index math is `(r - first_row_index) * (size of row) + (c - first_column_index)`.
- If rows are sequentially completed first during accessing elements in a two dimensional array, it is called row-major access. It is called column-major access for columns.

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
