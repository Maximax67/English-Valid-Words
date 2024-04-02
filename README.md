# English Valid Words

This repository contains CSV files with valid English words along with their frequency, stem, and stem valid probability.

## Files included

1. **valid_words_sorted_alphabetically.csv**:
    * N: Counter for each word entry.
    * Word: The English word itself.
    * Frequency count: The number of occurrences of the word in the 1-grams dataset.
    * Stem: The stem of the word.
    * Stem valid probability: Probability indicating the validity of the stem within the English language.

2. **valid_words_sorted_by_frequency.csv**:
    * Rank: The ranking of the word based on its frequency count.
    * Word: The English word.
    * Frequency count: The count of occurrences of the word in the 1-grams dataset.
    * Stem: The stem of the word.
    * Stem valid probability: Probability indicating the validity of the stem within the English language.

3. **valid_words.txt**: Txt file which contains valid words. Each word appears on a new line for convenient readability and usage.

## Data Collection Process

In order to curate a comprehensive dataset of valid English words, the following steps were undertaken:

1. **Initial Dataset**: I was searching a list of valid english words for my personal project and I found [this github repo](https://github.com/dwyl/english-words). However, to refine the dataset to meet my project specifications, a filtering process was necessary.

2. **Words Filtering**: I wrote the Words-filter.ipynb notebook to remove of words with non-alphabetical characters and words exceeding 25 characters.

3. **Frequency Data Collection**: To enrich the dataset with frequency information, the 1-grams dataset provided by Google was employed. Words with a frequency count less than 10,000 were removed.

4. **Stemming and Probability Calculation**: I used NLTK's Porter, Lancaster, and Snowball stemmers, along with a custom prefix stemmer to get stems with the highest frequency among all stemmers, which also existed in the dataset. Additionally, the probability of stem validity was calculated based on the frequencies of the original word and its stem. For further insights into the data curation process, please refer to the Valid-Word-List-Maker.ipynb file.


## License
This repository is released under the Unlicensed license. You are free to use, modify, and distribute the contents of this repository for any purpose without any restrictions.

## Acknowledgments
I would like to acknowledge the contributions of the following resources:

- [Word list by infochimps (archived)](https://web.archive.org/web/20131118073324/https://www.infochimps.com/datasets/word-list-350000-simple-english-words-excel-readable)
- [English words github repo by dwyl](https://github.com/dwyl/english-words)
- [The Google Books Ngram Viewer (used 1-grams dataset, version 20200217)](https://books.google.com/ngrams/)
- [NLTK (Natural Language Toolkit)](https://www.nltk.org/)
- [WordNet](https://wordnet.princeton.edu/)
