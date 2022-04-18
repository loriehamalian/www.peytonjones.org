---
title: "Making a faster curry with extensional types"
excerpt: "Paul Downen, Zachary Sullivan, Zena Ariola, Simon Peyton Jones <br><br> Published in <em>Haskell Symposium</em> by ACM
<br><br>
[View PDF](../assets/pdfs/making-a-faster-curry.pdf){: .btn .btn--info ..btn--large}
[Download BibTex](../assets/bibtex/making-a-faster-curry.bib){: .btn .btn--info ..btn--large}"
header:
    overlay_image: /assets/images/spj-stock-header.jpg
    overlay_filter: 0.5
permalink: /making-a-faster-curry-with-extensional-types/
tags:
  - publication
  - haskell
---

# Abstract
Curried functions apparently take one argument at a time, which is slow. So optimizing compilers for higher-order languages invariably have some mechanism for working around currying by passing several arguments at once, as many as the function can handle, which is known as its arity. But such mechanisms are often ad-hoc, and do not work at all in higher-order functions. We show how extensional, call-by-name functions have the correct behaviour for directly expressing the arity of curried functions. And these extensional functions can stand side-by-side with functions native to practical programming languages, which do not use call-by-name evaluation. Integrating call-by-name with other evaluation strategies in the same intermediate language expresses the arity of a function in its type and gives a principled and compositional account of multi-argument curried functions. An unexpected, but significant, bonus is that our approach is equally suitable for a call-by-value language and a call-by-need language, and it can be readily integrated into an existing compilation framework
