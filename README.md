# HSK Standard Course Vocabulary

This repo aims to have accurate digitized versions of the word lists at the back of the HSK standard coursebooks.

This could be useful for building flashcard decks or other learning resources.

## Current Status

This repo is a work in progress. The table below summarizes which of the word lists have been completed.

| HSK Coursebook | New Words | Proper Nouns | Words Not Included in the Syllabus | New Words Made Up of Characters Learned before | Supplementary Vocabulary |
|-----------|-----------|--------------|------------------------------------|------------------------------------------------|--------------------------|
| HSK 1     | ✘         | ✘            | ✘                                  | ✘                                              | ✘                        |
| HSK 2     | ✓         | ✘            | ✘                                  | ✘                                              | ✘                        |
| HSK 3     | ✓         | ✘            | ✘                                  | ✘                                              | ✘                        |
| HSK 4上   | ✓         | ✘            | ✘                                  | ✘                                              | ✘                        |
| HSK 4下   | ✓         | ✘            | ✘                                  | ✘                                              | ✘                        |
| HSK 5上   | ✓         | ✘            | ✘                                  | -                                              | -                        |
| HSK 5下   | ✓         | ✘            | ✘                                  | -                                              | -                        |
| HSK 6上   | ✘         | ✘            | ✘                                  | ✘                                              | ✘                        |
| HSK 6下   | ✘         | ✘            | ✘                                  | ✘                                              | ✘                        |

✓ = Done.
✘ = Not complete.
\- = Not applicable.

## Are the word lists accurate?

These lists were made with a combination of optical character recognition (OCR) and manual corrections. There may be errors in the word lists. I have not manually checked every single entry.

## I found a mistake!

If you find a mistake please email joel.laity@gmail.com and describe the mistake.

Alternatively, if you know how to use github then either (1) open an issue or (2) send a pull request fixing the mistake (or both!).

## How is this made?

For each HSK coursebook:

 1. Take a picture of each page in the back of the book that contains the word tables.
 1. Crop each of the columns in the tables except for the pinyin column. OCR does not work very well on pinyin so the pinyin is based on the character column.
 1. Use OCR to read each column. I use the Google Cloud Vision API.
 1. Manually correct anything the OCR got wrong.
 1. Use the [Dragon Mapper](https://dragonmapper.readthedocs.io/en/latest/) library to convert the characters into pinyin.
 1. Manually check the pinyin for all single character words. There are often multiple pronunciations for a single character, for example 得 can be pronounced dé, de or děi so the pinyin that Dragon Mapper outputs needs to be manually checked for single characters.
