# generating-names-rnn
### Generating Names with a Character-Level RNN using PyTorch

I followed [this](http://pytorch.org/tutorials/intermediate/char_rnn_generation_tutorial.html) tutorial from the PyTorch website and I extended it.

In this project:
* I used an [LSTM](http://colah.github.io/posts/2015-08-Understanding-LSTMs/) layer instead of their implementation of a recurrent layer using two linear layers
* I used [Embeddings](http://colah.github.io/posts/2014-07-NLP-RNNs-Representations/) instead of One-Hot Tensors
* I implemented [Beam Search](https://en.wikipedia.org/wiki/Beam_search)
* I used Adam optimizer

#### Usage
```
python train.py
python predict.py model
```

#### Requirements 
You need Python, PyTorch and Numpy
