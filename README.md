<!---
{
  "id": "2d349b37-ef59-4353-87e2-33896c7d0064",
  "depends_on": ["00650b50-14de-471d-a347-246f47ffadde"],
  "author": "Stephan Bökelmann",
  "first_used": "2025-06-02",
  "keywords": ["LaTeX", "mathematics", "equations", "vim", "math mode"]
}
--->

# Writing Mathematics in LaTeX

> In this exercise you will learn how to typeset mathematical expressions in LaTeX using inline and display math environments. Furthermore we will explore how to write fractions, superscripts, subscripts, square roots, and basic mathematical symbols.

### Introduction

One of LaTeX's most famous strengths is its capability to produce beautiful mathematical typesetting. Originally designed with scientific and mathematical publications in mind, LaTeX provides precise control over mathematical notation, enabling users to present formulas and equations with professional clarity.

Mathematics in LaTeX is written inside **math mode**, which differs from regular text mode. Entering math mode tells LaTeX to interpret special symbols and commands according to mathematical rules. There are two primary ways to enter math mode:

* **Inline math**: place math inside single dollar signs `$ ... $` to embed it within a paragraph.
* **Display math**: use either `\[ ... \]` or the `equation` environment to center and emphasize standalone equations.

LaTeX provides a wide range of commands for mathematical symbols and operations:

* Superscripts and subscripts using `^` and `_`
* Fractions using `\frac{numerator}{denominator}`
* Square roots with `\sqrt{}`
* Greek letters like `\alpha`, `\beta`, `\gamma`, etc.
* Operators like `\sum`, `\int`, and relational symbols such as `\leq`, `\geq`, `\neq`

Mastering math mode early opens the door to advanced topics like aligned equations, theorem environments, and complex mathematical structures required in scientific and technical writing. In this exercise, you will practice by writing both simple and moderately complex mathematical expressions.

### Further Readings and Other Sources

* [Overleaf: Mathematical Expressions](https://www.overleaf.com/learn/latex/Mathematical_expressions)
* [LaTeX Wikibook - Mathematics](https://en.wikibooks.org/wiki/LaTeX/Mathematics)
* [YouTube - LaTeX Math Typesetting Tutorial](https://www.youtube.com/watch?v=8SbKEP-mb6Q)
* [The Not So Short Introduction to LaTeX (Math Section)](https://tobi.oetiker.ch/lshort/lshort.pdf)

---

## Tasks

### Task 0: Create a New LaTeX File

Open Vim and create a new file:

```bash
vim math.tex
```

Insert the following base structure:

```latex
\documentclass{article}
\begin{document}

Your content goes here.

\end{document}
```

Save and exit Vim.

### Task 1: Write Inline Math Expressions

Replace `Your content goes here.` with:

```latex
\section{Inline Math}

The Pythagorean theorem states that $a^2 + b^2 = c^2$.
The quadratic formula is given by $x = \frac{-b \pm \sqrt{b^2 - 4ac}}{2a}$.
```

Compile using:

```bash
pdflatex math.tex
```

Verify that the formulas appear inline within the text.

### Task 2: Write Displayed Equations Using $ $

Add a new section below:

```latex
\section{Displayed Equations}

Here is the Pythagorean theorem displayed:

\[
a^2 + b^2 = c^2
\]

And the quadratic formula:

\[
x = \frac{-b \pm \sqrt{b^2 - 4ac}}{2a}
\]
```

Recompile and check that these are centered and properly formatted.

### Task 3: Use the Equation Environment with Automatic Numbering

Add another section:

```latex
\section{Numbered Equations}

\begin{equation}
E = mc^2
\end{equation}

\begin{equation}
\sum_{i=1}^{n} i = \frac{n(n+1)}{2}
\end{equation}
```

Recompile and verify that LaTeX numbers the equations automatically.

### Task 4: Insert Greek Letters and Operators

Extend your file with:

```latex
\section{Greek Letters and Operators}

Euler's formula:
\[
e^{i\pi} + 1 = 0
\]

An integral:
\[
\int_{0}^{\infty} e^{-x} dx = 1
\]

A summation:
\[
\sum_{k=1}^{10} k = 55
\]
```

Compile and verify correct rendering.

---

## Questions

1. What is the difference between inline and display math in LaTeX?
   Its easier to read and looks better organized
3. How do you write superscripts and subscripts?
   x^2 or x^{10}, x_1 or x_{10}
5. What is the purpose of the `equation` environment compared to `\[ \]`?
   with equation our formel gets number like (1), \[\...\\] not. 
7. How does LaTeX handle automatic equation numbering?
  when the file get compiled, compiler just counts equation elements and they get enumerated.
---

## Advice

Mathematical typesetting is where LaTeX truly shines. While the syntax may feel unfamiliar at first, the consistency and precision it provides are unmatched. Focus on understanding how math mode operates differently from text mode. Practice writing small formulas and gradually increase complexity. Use this knowledge to build documents that not only contain correct content but are also professionally formatted for publication and presentations. In the long run, mastering LaTeX math will save you time and frustration when preparing technical or academic documents.
