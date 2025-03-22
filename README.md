# Theory vs. Practice

- List 3 reasons why asymptotic analysis may be misleading with respect to
  actual performance in practice.

- Suppose finding a particular element in a binary search tree with 1,000
  elements takes 5 seconds. Given what you know about the asymptotic complexity
  of search in a binary search tree, how long would you guess finding the same
  element in a search tree with 10,000 elements takes? Explain your reasoning.

- You measure the time with 10,000 elements and it takes 100 seconds! List 3
  reasons why this could be the case, given that reasoning with the asymptotic
  complexity suggests a different time.

Add your answers to this markdown file.

# Questions & Answers

- List 3 reasons why asymptotic analysis may be misleading with respect to
  actual performance in practice.
  Asymptotic analysis focuses on how an algorithm behaves for large input sizes,
  so when dealing with small data sets, an algorithm with poorer asymptotic
  runtime could out perform an algorithm that theoretically, based on asymptotic
  runtime, should run faster. An example of this discussed in class is insertion
  sort, $O(n^2)$, out performing quick sort, $O(nlog n)$, with small data sets.
  Asymptotic analysis doesn't account for constants, and bases its performance
  exclusively on the dominant term. For example an algorithm with a complexity
  of $4n^2+n$ gets baked down to $O(n^2)$. Sure, as our data set approaches
  an infinite quantity of entries, those constants and lower order terms mean
  very little, but in the real world those eccentricities still mean something.
  Asymptotic analysis doesn't account for what language a program is written in.
  Broadly speaking different programming languages are capable of performing the
  same tasks; however, they perform these tasks with different efficacies. A
  significant distinction is compiled vs interpreted languages. Compiled
  languages typically offer better performances, and even amongst all compiled
  languages, each will have different performance capabilities. Though
  insignificant with small data sets, the same algorithm sorting the same data
  in C vs Python, when sorting large data sets, could result in dramatically
  different real world performances.

  - Suppose finding a particular element in a binary search tree with 1,000
  elements takes 5 seconds. Given what you know about the asymptotic complexity
  of search in a binary search tree, how long would you guess finding the same
  element in a search tree with 10,000 elements takes? Explain your reasoning.

- You measure the time with 10,000 elements and it takes 100 seconds! List 3
  reasons why this could be the case, given that reasoning with the asymptotic
  complexity suggests a different time.
