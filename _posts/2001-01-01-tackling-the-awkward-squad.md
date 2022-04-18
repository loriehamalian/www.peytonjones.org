---
title: "Tackling the awkward squad: monadic input/output, concurrency, exceptions, and foreign-language calls in Haskell"
excerpt: "Simon Peyton Jones <br><br>  Published in <em>Engineering Theories of Software Construction</em> by IOS Press, ISBN: ISBN 1 58603 1724
<br><br>
[View PDF](../assets/pdfs/tackling-awkward-squad.pdf){: .btn .btn--info ..btn--large}
[Download BibTex](../assets/bibtex/tackling-awkward-squad.bib){: .btn .btn--info ..btn--large}"
header:
    overlay_image: /assets/images/spj-stock-header.jpg
    overlay_filter: 0.5
hidden: true 
permalink: /Tackling-the-awkward-squad/
tags:
  - haskell
  - publication
---

# Abstract
I’ve revised the notes significantly, with the help of feedback from many people. Last update: 21 Feb 2001.

  - [PowerPoint slides](../assets/ppts/Marktoberdorf.ppt)
  - [Writing High-Performance Server Applications in Haskell, Case Study: A Haskell Web Server](https://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.37.3257), Simon Marlow, Haskell Workshop, Montreal, Canada, Sept 2000. This paper describes the running example in the notes.

This tutorial focuses on explaining the “bits round the edges” of Haskell programs, rather than the beautiful functional core we all know and love. More specifically, it gives, in a single framework, an account of
  - monadic input/output (the I/O monad)
  - concurrency (threads, MVars)
  - exceptions (both synchronous and asynchronous)
  - foreign language interfaces

The common feature of all of these is, of course, the ubiquitous I/O monad. All except the first (basic I/O) involve proposed extensions to Haskell that are implemented in GHC, and I have tried hard to make the tutorial use exactly the same function names as GHC does. All of the extensions are described in conference papers (also available from my home page), but these papers are not tutorials, and were written with varying nomenclature over a period of several years. I hope that this tutorial gives a more comprehensible overview of the big picture, using a common vocabulary.

The tutorial also gives an operational semantics for everything described except the foreign-language interface part. For this I borrow the framework of operational semantics — but don’t worry! My intention is that you don’t need to know a thing about operational semantics to understand the paper.

I occasionally update this tutorial, and I would very much appreciate your help in improving it. If you read it, please let me know of any errors you find and suggestions for improvement.
