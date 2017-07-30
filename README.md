# generating-names-rnn
### Generating Names with a Character-Level RNN using PyTorch

I followed [this](http://pytorch.org/tutorials/intermediate/char_rnn_generation_tutorial.html) tutorial from the PyTorch website and I extended it.

In this project:
* I used an [LSTM](http://colah.github.io/posts/2015-08-Understanding-LSTMs/) layer instead of their implementation of a recurrent layer using two linear layers
* I used [Embeddings](http://colah.github.io/posts/2014-07-NLP-RNNs-Representations/) instead of One-Hot Tensors
* I implemented [Beam Search](https://en.wikipedia.org/wiki/Beam_search)
* I used Adam optimizer
* I added the Start of Sentence token so that sampling can be done without choosing a starting letter

#### Usage
```
python train.py
python predict.py model
```

#### Requirements 
You need Python, PyTorch and Numpy

#### Some results (beam size 3)
```
====== Irish
O'Dell -0.6350323756535848
O'Brian -0.6820564951215472
O'Brien -0.6878840582711356
====== Italian
Albero -0.9236377875010172
Alberigo -0.8406117558479309
Alberighi -0.6255239380730523
====== Scottish
Watson -0.5849217971165975
Walker -0.623577872912089
Sutherland -0.4097114562988281
====== Korean
Son -1.195298433303833
Shin -0.8101678490638733
Choe -1.0431489944458008
====== English
Keeley -1.2196478048960369
Hellan -1.322618802388509
Keeling -1.1574227469308036
====== Arabic
Samaha -0.5359944899876913
Haddad -0.6641473372777303
Shamoon -0.670792715890067
```

