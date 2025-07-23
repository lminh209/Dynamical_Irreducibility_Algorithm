# An Algorithm for Determining the Dynamical Irreducibility of Cubic Polynomials over Finite Fields


## Table of Contents

  - [Description](#description)
  - [What you can find here](#what-you-can-find-here)
  - [Using the Algorithm](#using-the-algorithm)
  - [Reflections](#reflections)
  - [Acknowledgement](#acknowledgement)
  - [Reference](#reference)

## Description

**Tech used:** Magma

This algorithm was developed as part of the research project on Dynamical Irreducibiilty of Polynomials over Finite Fields at Mount Holyoke College, done under the mentorship of Professor Tori Day.

It is used for determining if a cubic polynomial of the form f(x) = ax^3 + bx^2 + cx + d is dynamically irreducible over a given finite field of order q (q being a prime or prime power), and is based on a Sage algorithm for determining the dynamically irreducibility of polynomials of the form f(x) = ax^3 + cx + d (Day, Deland, Juul, Thomas, Thompson, Tobin).

## What you can find here

Here is a brief guide for navigating through the repository.

* In the [algorithm_versions](https://github.com/lminh209/Algorithm1/tree/main/algorithm_versions) folder, you will find the code for the algorithm and its helper functions.
* In the [test](https://github.com/lminh209/Algorithm1/tree/main/test) folder, you will find some functions for performing automated tests on the algorithm.

## Using the Algorithm

If you haven't installed Magma on your computer, here is a guide for that: [Installation Instructions](https://magma.maths.usyd.edu.au/magma/faq/install)

If you have installed Magma, follow these steps to use the algorithm:

1. Download the files Helper_Functions.txt, Algorithm1_v4.txt and Algorithm2_v2.txt in the folder [algorithm_versions](https://github.com/lminh209/Algorithm1/tree/main/algorithm_versions).
2. Open Magma, then load the previously downloaded files into Magma in this order: Helper_Functions.txt -> Algorithm1_v4.txt -> Algorithm2_v2.txt.
  You can do that using this Magma command:
    ```
    load "filepath"; // paste the filepath for the file you want to load in between the quotation marks
   ```
The algorithm should now be ready to use! You can test it out on creating a polynomial of your choice, like so:

**Example:**

```
// Create polynomial over finite field of order 7
F:=FiniteField(7);
P<x>:=PolynomialRing(F);
f:=x^3+2*x^2+x+1;

// Check if polynomial f is dynamically irreducible over 5 iterations
Algorithm2(f, 7, 5, 1);
```


## Reflections

Through this project, I was involved in math research for the first time - which led to a series of other first-times: learning Magma, presenting about out research at MHC math lunch, and finding out how fun math can be!

The research process was a great learning opportunity. Through weeks of reading theories, coding, testing, debugging, I had the chance to expand my comfort zone, step by step.

* I practiced breaking down into pieces a problem that seemed daunting at first sight, and solving it piece by piece.
* I found two new tools for tackling problems: composure and confidence. A lot of times, bugs that were confusing at first can be fixed by letting myself take time, and believing there was a solution to be found.
* I learned to voice my questions and concerns - and was truly grateful to be among great people who are willing to give me support and guidance ☺️

## Acknowledgement

I would like to express my gratitude for Mount Holyoke College's Math/Stat/Data Department for supporting this summer research project.

I also want to thank Professors Tony Liu and Chassidy Bozeman, whom I took Data Structures and Discrete Math with. The coding and proofwriting skills I learned from your classes proved useful in this project!

Lastly, I want to thank my mentor, Professor Tori Day, for giving me the opportunity to be involved in the project and . I learned a lot from your knowledgeableness, enthusiasm and patience.

## Reference

1. Tori Day, Rebecca Deland, Jamie Juul, Cigole Thomas, Bianca Thompson, and Bella Tobin, "Dynamical Irreducibility of Certain Families of Polynomials over Finite Fields" (2024). https://arxiv.org/abs/2409.10467.