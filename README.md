greek_syllabes

Βιβλιοθήκη για να μετρά Ελληνικές συλλαβές. Δεν συλλαβίζει με ακρίβεια, αλλα μετρά τις συλλαβές σωστά. 

This is a library that counts the number of syllabes in greek text by batching letters around vowels/valid vowel clusters and counting the batches. It doesn't syllabize properly in regards to the consonants, but if you want to implement it it's a pretty easy fix. It just needs a dictionary of the consonant groups that have words starting from them so you can batch at valid consonant clusters and a rule to divide twin letters in their respective syllabes. 

Available functions are listed in main.
