---
layout: post
title: Mathjax Test
subtitle: My first mathjax expression
categories: markdown
tags: [test]
---

* A safe integer is an integer that
  * can be exactly represented as an IEEE-754 double precision number, and
  * whose IEEE-75 representation cannot be the result of rounding any other integer to fit the IEEE-754 representation
* For example, $ 2 ^ {53} - 1 $ is a safe integer,
  * it can be exactly represented 


<!-- Block math, keep all blank lines -->

$$
LaTeX_math_expression
$$

<!-- Equation numbering, keep all blank lines  -->

$$
\begin{equation}
  LaTeX_math_expression
  \label{eq:label_name}
\end{equation}
$$

Can be referenced as \eqref{eq:label_name}.

<!-- Inline math in lines, NO blank lines -->

"Lorem ipsum dolor sit amet, $$ LaTeX_math_expression $$ consectetur adipiscing elit."

<!-- Inline math in lists, escape the first `$` -->

1. \$$ LaTeX_math_expression $$
2. \$$ LaTeX_math_expression $$
3. \$$ LaTeX_math_expression $$
