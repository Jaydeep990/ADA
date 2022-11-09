# String Matching

## Naive String Matching Algorithm
 
- Given a text of length N txt[0..N-1] and a pattern of length M pat[0..M-1]
- We need to find all occurrences of pat[] in txt[].
- You may assume that N > M.

```
Input:  txt[] =  “AABAACAADAABAABA”, pat[] =  “AABA”
Output: Pattern found at index 0, Pattern found at index 9, Pattern found at index 12
```

<img src="https://media.geeksforgeeks.org/wp-content/uploads/20220809155713/image-660x398.png" width=50%>

- Slide the pattern over text one by one and check for a match. 
- If a match is found, then slide by 1 again to check for subsequent matches. 
#### Algorithm
```
NAIVE-STRING-MATCHER (T, P)
 1. n ← length [T]
 2. m ← length [P]
 3. for s ← 0 to n -m do
 4.   if P [1.....m] = T [s + 1....s + m]
 5.     then print "Pattern occurs with shift" s
```
#### Best Case
- The number of comparisons in the best case is O(N). 
- The best case occurs when the first character of the pattern is not present in the text at all.
```
txt[] = "AABCCAADDEE";
pat[] = "FAA";
```

#### Worst Case
- The number of comparisons in the worst case is O(M * (N – M + 1)).
- The worst case of Naive Pattern Searching occurs in the following scenarios. 
- 1) When all characters of the text and pattern are the same. 
- 2) Worst case also occurs when only the last character is different. 

```
1. 
txt[] = "AAAAAAAAAAAAAAAAAA";
pat[] = "AAAAA";
2.
txt[] = "AAAAAAAAAAAAAAAAAB";
pat[] = "AAAAB";
```

## Rabin-Karp Algorithm
- Given a text of length N txt[0..N-1] and a pattern of length M pat[0..M-1]
- We need to find all occurrences of pat[] in txt[].
- You may assume that N > M.

```
Input:  txt[] =  “AABAACAADAABAABA”, pat[] =  “AABA”
Output: Pattern found at index 0, Pattern found at index 9, Pattern found at index 12
```
<a href="https://www.baeldung.com/wp-content/ql-cache/quicklatex.com-d2c361d29aba6b82663b3e7f608f35e9_l3.svg"> SVG for better understanding </a>
<br>
<img src="https://www.baeldung.com/wp-content/ql-cache/quicklatex.com-d2c361d29aba6b82663b3e7f608f35e9_l3.svg" width=50%>
<br>

- Rabin-Karp algorithm is an algorithm used for searching/matching patterns in the text using a **hash function**.
- A hash function is a tool to map a larger input value to a smaller output value. This output value is called the **hash value**.

#### Working of Rabin-Karp Algorithm

- A sequence of characters is taken and calculate hash value and compare with required string's hash value.
- If the hash value is same then, character matching is performed.

#### Example

<a href="https://www.programiz.com/dsa/rabin-karp-algorithm">Link</a>

#### (Spurious Hit) Limitations of Rabin-Karp Algorithm

- When the hash value of the pattern matches with the hash value of a window of the text but the window is not the actual pattern then it is called a spurious hit.
- Spurious hit increases the time complexity of the algorithm. In order to minimize spurious hit, we use modulus. It greatly reduces the spurious hit.

#### Rabin-Karp Algorithm Complexity

- The average case and best case complexity of Rabin-Karp algorithm is O(m + n) and the worst case complexity is O(mn).
- The worst-case complexity occurs when spurious hits occur a number for all the windows.

#### Rabin-Karp Algorithm Applications

- For pattern matching
- For searching string in a bigger text

## Finite Automata

## KMP (Knuth Morris Pratt) Algorithm

- Given a text of length N txt[0..N-1] and a pattern of length M pat[0..M-1]
- We need to find all occurrences of pat[] in txt[].
- You may assume that N > M.

```
Input:  txt[] =  “AABAACAADAABAABA”, pat[] =  “AABA”
Output: Pattern found at index 0, Pattern found at index 9, Pattern found at index 12
```

#### KMP overview
- KMP algorithm is used to find a "Pattern" in a "Text". 
- This algorithm campares character by character from left to right. - But whenever a mismatch occurs, it uses a preprocessed table called "Prefix Table" to skip characters comparison while matching.

#### **Components of the KMP algorithm:**
1. Prefix.
2. Suffix.
3. LPS table : Table for detecting the Longest Proper Prefix that is also a Suffix



##### **Time Complexity**: O(n) in the worst case where n is the length of text.
##### **Space Complexity**: O(m) where m is the size of the pattern.

##### **Advantages of the KMP algorithm**
- A very obvious advantage of the KMP algorithm is it's time complexity. It's very fast as compared to any other exact string matching algorithm.

##### **Disadvantage of the KMP algorithm**
- The only disadvantage of the KMP algorithm is that it is very complex to understand.

##### **Applications of the KMP Algorithm**
1. Search engines
2. Searching content in large databases
3. Spam filters
4. Spelling checkers
5. Digital Forensics

<img src="https://scaler-topics-articles-md.s3.us-west-2.amazonaws.com/kmp-algorithm-lps-table.gif">
