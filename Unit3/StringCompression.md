### String Compression Intro

#### Task 1 - Disemvoweling

Write a function in Java or JavaScript that removes all the vowels from a String.

#### Task 2 - Simple compression

Given a string that looks like **aaaabbbbbhhhhhttttttrrrrrr**, write a program that compresses the string by indicating how many sequential occurrences of a letter there are in a row. E.g.:

`aaaabbbbbhhhhhttttttrrrrrr -> a4b5h4t6r6`

### Task 3 (Day 2 Challenge)- Dictionary compression

Given a string of text with repeating words or phrases, write a program that:
1. Allows a user to enter a phrase to compress 
2. adds that phrase to the dictionary under a numerical key
3. displays the text with the key replacing each instance of the phrase
4. displays the dictionary in a pleasing form
5. Calculates the compression rate as follows and displays it to the screen: 
(length of original text - length of compressed text + number of keys in Dict + length of strings Values in Dict) /length of original text

Bonus features:

* allow the user to remove keys from the dictionary
* allow the user to create a dictionary entry from text that contains a mix of plain text and dictionary keys (think escape characters)
