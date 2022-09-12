## GSoC with TensorFlow (Keras Team)

Hey!

Thanks for checking out my work

First things first I'm really thankful to Google for organizing this wonderful event every year and also huge thanks to the TensorFlow-Keras Team for having me on the team and to my mentors 
[Matthew Watson](https://github.com/mattdangerw) and [Chen Qian](https://github.com/chenmoneygithub) who helped me throughout the journey.

My work mainly focused on contributing to KerasNLP a new library which is currently pre-release and aims to build "Industry-strength Natural Language Processing workflows with Keras"

I started contributing to the library in March 2022 and really liked the codebase as it was pretty easy to navigate through and the maintainers were really helpful in guiding beginners!

I mainly worked towards adding Data Augmentation Techniques, tokenizers and tokenizer training utilities, fixing bugs, adding new options to pre-existing utilities and writing tutorials for `keras.io`

My PRs:

## Data Augmentation Techniques

| PR Link   |      Status      |  Description |
|----------|:-------------:|------:|
| [Random Deletion Layer](https://github.com/keras-team/keras-nlp/pull/214) |  Merged | Adds the Random Deletion operation as a Keras Layer described in the paper [EDA: Easy Data Augmentation Techniques for Boosting Performance on Text Classification Tasks](https://arxiv.org/pdf/1901.11196.pdf) |
| [Random Swap Layer](https://github.com/keras-team/keras-nlp/pull/224) |  Merged | Adds the Random Swap operation as a Keras Layer described in the paper [EDA: Easy Data Augmentation Techniques for Boosting Performance on Text Classification Tasks](https://arxiv.org/pdf/1901.11196.pdf) |
| [Random Replacement Layer](https://github.com/keras-team/keras-nlp/pull/274) | In Review | Adds the Random Replacement operation as a Keras Layer described in the paper [EDA: Easy Data Augmentation Techniques for Boosting Performance on Text Classification Tasks](https://arxiv.org/pdf/1901.11196.pdf) |
| [Random Insertion Layer](https://github.com/keras-team/keras-nlp/pull/235) | In Review | Adds the Random Insertion operation as a Keras Layer described in the paper [EDA: Easy Data Augmentation Techniques for Boosting Performance on Text Classification Tasks](https://arxiv.org/pdf/1901.11196.pdf) |
| [Minor fixes to the Random Deletion Layer](https://github.com/keras-team/keras-nlp/pull/286) | Merged | Fixed some minor bugs in the Deletion Layer |
| [Docstring and Test Fixes for Random Deletion Layer](https://github.com/keras-team/keras-nlp/pull/339) | Merged | Made fixes in the Random Deletion Layer to improve docstring and remove redundancy in tests |

The work was majorly aimed towards adding support for Data Augmentation Techniques in the form of Keras Pre-Processing Layers. The Layers are graph mode compatible as well and hence work with tf datasets which are more efficient. The layers also provide granular control such as deciding which tokens to skip using a list, a tf function or even a native python function. Insertion and Replacement layers also have fine grained control over how to choose the new token using either a list, a tf function or a native python function.

Major portion of my GSoC timeline went towards this work as this included several API redesigns to make it usable for the end users and also needed to be graph mode compatible to be usable with tf datasets

## Tokenizers

| PR Link   |      Status      |  Description |
|----------|:-------------:|------:|
| [Fixes for the WordPieceTrainer](https://github.com/keras-team/keras-nlp/pull/293) | Merged | These tests removed dependency between tests in the docstring and those in the test files for file handling |
| [Created a trainer for SentencePiece Tokenizer](https://github.com/keras-team/keras-nlp/pull/281) | Merged | Added a trainer which Trains a SentencePiece vocabulary from an input dataset or a list of filenames. |
| [Fixed Bug in Unicode Tokenizer Vocab Size](https://github.com/keras-team/keras-nlp/pull/243) | Merged | Fixed bug caused by mistake in argument name |
| [Added a vocabulary_size argument to UnicodeCharacterTokenizer](https://github.com/keras-team/keras-nlp/pull/163) | Merged | Incorporated capping OOV tokens in the UnicodeCharacterTokenizer by setting vocabulary_size |
| [Adding Utility to Detokenize as list of Strings to Tokenizer Base Class](https://github.com/keras-team/keras-nlp/pull/124) | Merged | Added a utility which decodes tensors into list of strings over bytestring recursively |
| [UnicodeCharacterTokenizer ](https://github.com/keras-team/keras-nlp/pull/100) | Merged | Added a new tokenizer for tokenization into Unicode Characters |
| [Fixing rank 1 outputs for WordPieceTokenizer ](https://github.com/keras-team/keras-nlp/pull/92) | Merged | Fixed issue with Rank 1 outputs in WordPieceTokenizer |

Tokenizers are an essential part of any NLP Library. KerasNLP also has its share of tokenizers. I majorly contributed to the building of the UnicodeCharacterTokenizer, some fixes for WordPieceTokenizer and Trainer and creating a utility to train create proto files for SentencePiece Tokenizer.

## BERT Model Related Work

| PR Link   |      Status      |  Description |
|----------|:-------------:|------:|
| [Adding Eval Script for BERT on SQUAD Dataset](https://github.com/keras-team/keras-nlp/issues/285)| In Works | Aims to add an Eval Script for BERT on SQUAD Dataset |
| [Migrating from Datasets to TFDS for GLUE Example](https://github.com/keras-team/keras-nlp/pull/340) | Merged | Removed dependency on Datasets for GLUE and instead migrated to TFDS |

This work is mainly towards adding more features to the BERT model present in the repository which makes it easy for the end user to rebuild models by modifying the code. I worked towards changing dataset dependency and also I'm currently working on adding an Eval Script for SQUAD Dataset.

## Guides

| PR Link   |      Status      |  Description |
|----------|:-------------:|------:|
| [Guide on Open Ended Text Generation Guide KerasNLP](https://github.com/keras-team/keras-io/pull/956) | In Review | Added a guide for `keras.io` which showcases tradeoff between Byte and Unicode Tokenizer |

This guide aims to showcase our tokenizers to the end-users and also attract attention towards the library

## General Work

| PR Link   |      Status      |  Description |
|----------|:-------------:|------:|
| [Added Debug Info for Line Ending Issues ](https://github.com/keras-team/keras-nlp/pull/64) | Merged | Added some documentation to address issues caused while running linters in wrong file ending mode |
| [Fixed Import Error ](https://github.com/keras-team/keras-nlp/pull/161) | Merged | Fixed error caused by missing init file |
| [Fixed Import for top_p_search util ](https://github.com/keras-team/keras-nlp/pull/245) | Merged | Fixed error caused by missing import in init file for top_p_search |
| [Added Kernel and Bias Initializers](https://github.com/keras-team/keras-nlp/pull/50) | Merged | Added Kernel and Bias Initializers to Encoder and Decoder classes |
<<<<<<< HEAD

These are minor bugs and fixes along with some basic features which I worked towards fixing/adding.

=======
>>>>>>> 365e3d0675b625e752f05d06cb296409e4864ad1
