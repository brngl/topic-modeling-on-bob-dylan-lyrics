# Topic Modeling on Bob Dylan lyrics

Lyrics texts are provided by this project:
https://github.com/mulhod/bob_dylan_lyrics

It's performed LDA on Bob Dylan lyrics using a variable number of topics.

For each LDA run with a different number of topics, it's shown a word cloud created taking in count the words that appears in topics and their scores. The word cloud is created from a text file containing the words from topics. Every word has an occurence in the text dicrectly proportional to his score in his topic of origin.

### Input creation
The first step is the creation of the input. It is a text file in which every row corresponds to a lyric in plain. For each replicated lyric (for example the ones that belong to different albums or different versions of the same song), it's took just a copy. Lyrics source is a set of .txt files in which every file is a lyric.

### Preprocessing
The input is cleaned up from english stopwords. Beyond the usual english stopwords, are eliminated names of persons, name of places and words belonging to english slang.

After that, it's used a TF-IDF function to delete less relevant words.

- Stemming: the excecution is performed both with word stemming and without, so, for the first case, it's applied a stemming by Porter to the document.

The corpus thus obtained could be saved in a text file.

### Execution
LDA is performed both with Porter stemming and without. For both cases are made different runs with a different number of topic.

At the end of each run are shown topics and their respective word clouds.

