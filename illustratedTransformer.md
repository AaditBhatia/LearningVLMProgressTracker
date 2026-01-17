https://jalammar.github.io/illustrated-transformer/

It started with a link to https://jalammar.github.io/visualizing-neural-machine-translation-mechanics-of-seq2seq-models-with-attention/, so why not do that first?

A sequence-to-sequence model is a model that takes a sequence of items (words, letters, features of an images…etc) and outputs another sequence of items. 

Under the hood, the model is composed of an encoder and a decoder.

The encoder processes each item in the input sequence, it compiles the information it captures into a vector (called the context). After processing the entire input sequence, the encoder sends the context over to the decoder, which begins producing the output sequence item by item.

Encoder and Decoder are RNN's : https://www.youtube.com/watch?v=UNmqTiOnRfg(for later)

Question - The author says in the real world, the size of a context window can be 256/512/1024. What happens with a bigger context window size?

RNN takes 2 inputs by design: input + hidden State and returns an output + hidden State

So how a Sequence to sequence model will work is it will take an input, send it through the encoder and decoder. The encoder passes in a context vector to the decoder. Earlier(Pre-attention), this context vector was passed in through every layer of the encoder and every layer of the decoder. 

However, for large sequences, this quickly became a bottleneck.  Attention allows the model to focus on the relevant parts of the input sequence as needed.

Attention encoder now passses all the hidden states to the decoder. The decoder, to find relevant info, takes in all the hidden states, and gives each hidden state a score. The score is then softmaxed, and each vector is multiplied by its softmaxed score. This amplifies relevant results
