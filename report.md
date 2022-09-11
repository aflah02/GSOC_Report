## GSoC with TensorFlow (Keras Team)

Hey!

Thanks for checking out my work

First things first I'm really thankful to Google for organizing this wonderful event every year and also huge thanks to the TensorFlow-Keras Team for having me on the team and to my mentors 
[Matthew Watson](https://github.com/mattdangerw) and [Chen Qian](https://github.com/chenmoneygithub) who helped me throughout the journey.

My work mainly focused on contributing to KerasNLP a new library which is currently pre-release and aims to build "Industry-strength Natural Language Processing workflows with Keras"

I started contributing to the library in March 2022 and really liked the codebase as it was pretty easy to navigate through. 

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