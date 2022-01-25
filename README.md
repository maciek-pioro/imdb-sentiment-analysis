# imdb-sentiment-analysis
Mark IMDB reviews as either positive or negative using stacked LSTMs.
Facilitate learning and testing by using Pytorch Lightning.
Log data with ClearML.
## Examples of sentences from test set

## Model performance


## Future improvement directions
There is a number of possible approaches which could both raise the test accuracy and speed up the training process
  - Use of pretrained word embeddings: this is a standard approach in the field of NLP. The current approach tries to learn word embeddings on its own which is a time-consuming task. At the same time there is not enough data in the IMDB dataset to achieve SOTA performance. There are various pre-trained word embeddings available under permissive licensing schemes such as Word2Vec by Google or GloVe from Stanford University.
  - Elimination of rare tokens: words which are not used often (e. g. [_hapax legomena_](https://en.wikipedia.org/wiki/Hapax_legomenon)) do not carry any meaningful information which the model could learn on its own. The usefulness of this approach would be diminished if pre-trained embeddings were used.
  - Use of transformers: LSTM is not regarded anymore as a SOTA neural net architecture. Currently, the most powerful NLP models commonly use transformers, which adopt the mechanism of self-attention, i. e. they focus only on the parts of the input which seems the most important for the task at hand.
