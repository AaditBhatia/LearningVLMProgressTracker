https://jalammar.github.io/illustrated-transformer/

It started with a link to https://jalammar.github.io/visualizing-neural-machine-translation-mechanics-of-seq2seq-models-with-attention/, so why not do that first?

A sequence-to-sequence model is a model that takes a sequence of items (words, letters, features of an images…etc) and outputs another sequence of items. 

Under the hood, the model is composed of an encoder and a decoder.

The encoder processes each item in the input sequence, it compiles the information it captures into a vector (called the context). After processing the entire input sequence, the encoder sends the context over to the decoder, which begins producing the output sequence item by item.

Encoder and Decoder are RNN's : https://www.youtube.com/watch?v=UNmqTiOnRfg(for later)

Question - The author says in the real world, the size of a context window can be 256/512/1024. What happens with a bigger context window size?

RNN takes 2 inputs by design: input + hidden State and returns an output + hidden State


