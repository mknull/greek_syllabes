greek_syllabes

Βιβλιοθήκη για να μετρά Ελληνικές συλλαβές. Δεν συλλαβίζει με ακρίβεια, αλλα μετρά τις συλλαβές σωστά. 

This is a library that counts the number of syllabes in greek text by batching letters around vowels/valid vowel clusters and counting the batches. It doesn't syllabize properly in regards to the consonants, but if you want to implement it it's a pretty easy fix. It just needs a dictionary of the consonant groups that have words starting from them so you can batch at valid consonant clusters and a rule to divide twin letters in their respective syllabes. 

Available functions:

-------------------
Vowel manipulation
-------------------

is_fonien(word,n):                   #Ask if a specific letter is a vowel. Requires the word iteration index (n).
#                                         Returns True/False
is_2nd_fonien(single word,n)         #Ask if this letter and the next make up a valid vowel cluster.
#                                         Returns True/False
is_3rd_fonien(single word,n)         #Ask if this letter, the next and the one after make up a valid vowel cluster.
#                                         Returns True/False
identify_fonien_block(single word,n) #Feed it a vowel and get back a string with a valid vowel cluster starting from the vowel
last_fonien(single word,n)           #Ask if the vowel you fed it is the last fonien in the word. 
#                                         Returns True/False

-------------------
Word manipulation
-------------------

wordify(some input) breaks input into words and returns a list made of the words
syllabize_word(single word)          #Feed it a word and get a string with a hyphen or space separating each syllable
syllabize_sentences(whatever)        #Feed it whatever and it will apply wordify() and syllabize_word() to get you
#                                       a string of the whole input with a hyphen or space separating each syllabe

----------
statistics
----------

count_my_syllabes(output)            #Intended to be used on the output of syllabize_sentences(). Returns the number 
#                                    # of syllabes, words and sentences (actually just counts the periods so beware
#                                    # of triple dots (...)

