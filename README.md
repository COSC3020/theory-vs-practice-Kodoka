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

## Question 1
  
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

## Question 2

  A BST has a asymptotic complexity of $O(log_{2} n)$. Knowing that $T(n)$ for
  $n=1000$ takes 5 seconds, we can calculate a ratio, $c$, by which we can
  calculate $T(10000)$.  
  $c \cdot \log_{2} 1000 = 5$  
  $c = frac{5}{\log_{2} 1000}$  
  Using that ratio, $c$  
  $T(10000) = frac{5}{\log_{2} 1000} \cdot \log(10000)$  
  $T(10000) \approx 0.5017 \cdot 13.2877$  
  $T(10000) \approx 6.6664$  
  Thus, I'd guess T(10000) would take 6.6664 seconds.  

- You measure the time with 10,000 elements and it takes 100 seconds! List 3
  reasons why this could be the case, given that reasoning with the asymptotic
  complexity suggests a different time.  

# Resources

I read through the following for a broad overview of the differences between compiled and interpreted languages, for my third reason why asymptotic analysis may be misleading:  
https://www.geeksforgeeks.org/difference-between-compiled-and-interpreted-language/#

# Plagiarism Notice

I certify that I have listed all sources used to complete this exercise, including the use of any Large Language Models. All of the work is my own, except where stated otherwise. I am aware that plagiarism carries severe penalties and that if plagiarism is suspected, charges may be filed against me without prior notice.
