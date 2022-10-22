# Compounded-Words

A compounded word is one that can be constructed by combining (concatenating) shorter words also found in the same file
Reads provided files (Input_01.txt and Input_02.txt) containing alphabetically sorted words list (one word per line, no spaces, all lower case)
Identifies & display below given data in logs/console/output file
*Longest compounded word
Second longest compounded word
Time taken to process the input file*

Approach:
Every string is traversed character by character. Trie (prefix) tree is used to keep track of all the valid words in a compound word. Trie tree gives a O(n) search-time for a word, where 'n' is word length. 

To check if a word is a compound word, the program traverses the string character by character, till it finds a complete word from the trie. It then recursively checks whether the remaining part is also a word OR a compound word.

The worst-case time complexity to check whether a word is compound is O(n^2), where 'n' is word length. Hence, for 'm' words, the time complexity is O(m.n^2). The word length 'n' is very small for a large dataset.
