---
layout: post
title: Data Jam ep 5 - Positional Encoding in Transformer
---

In languages, the order of the words and their position in a sentence really matters.

The meaning of the entire sentence can change if the words are re-ordered. When implementing NLP solutions, recurrent neural networks have an inbuilt mechanism that deals with the order of sequences. The transformer model, however, does not use recurrence or convolution and treats each data point as independent of the other.

As we can see from the title, Attention Is All You Need, Transformers fully replace the recurrent units with attention.

Unlike the recurrent unit, the attention computation across tokens can be fully parallelized, that is, they do not have to wait for the calculation of the previous token’s representation to get the current token’s representation.

However, in return for the grace of parallelization, Transformers gave up the inductive bias of recurrence that RNNs have. Without positional encoding, the Transformer is permutation-invariant as an operation on sets.

For example, “Alice follows Bob” and “Bob follows Alice” are completely different sentences, but a Transformer without position information will produce the same representation. Therefore, the Transformer explicitly encodes the position information.

Hence, positional information is added to the model explicitly to retain the information regarding the order of words in a sentence. Positional encoding is the scheme through which the knowledge of the order of objects in a sequence is maintained.

## What Is Positional Encoding?
Positional encoding describes the location or position of an entity in a sequence so that each position is assigned a unique representation.

## Why use sine and cosine functions?
There are many reasons why a single number, such as the index value, is not used to represent an item’s position in transformer models. For long sequences, the indices can grow large in magnitude. If you normalize the index value to lie between 0 and 1, it can create problems for variable length sequences as they would be normalized differently.

In order not to use a sequence of integers (1, 2, 3, ... n) because of the lack of boundary in the value and the magnitude, a float friendly is preferred. But, just using a limited (0 to 1) option means you need to know the length of the sequence beforehand.
This is why the authors propose a cyclic solution. Sin and cos functions can benefit from this idea and thus are the choice here. But why using both instead of one?


## The Intuition
You may wonder how this combination of sines and cosines could ever represent a position/order? It is actually quite simple, Suppose you want to represent a number in binary format, how will that be?

You can spot the rate of change between different bits. The LSB bit is alternating on every number, the second-lowest bit is rotating on every two numbers, and so on.

But using binary values would be a waste of space in the world of floats. So instead, we can use their float continous counterparts - Sinusoidal functions. Indeed, they are the equivalent to alternating bits. Moreover, By decreasing their frequencies, we can go from red bits to orange ones.

## History
- Absolute Position Encodings Explained | Papers With Code
- Relative Position Encodings Explained | Papers With Code
- Rotary Embeddings Explained | Papers With Code.
- ALiBi Explained | Papers With Code

## References
- A Short History of Positional Encoding - Dongkwan Kim
- A Gentle Introduction to Positional Encoding in Transformer Models, Part 1 - MachineLearningMastery.com.
- Transformer Architecture: The Positional Encoding - Amirhossein Kazemnejad's Blog
- Master Positional Encoding: Part I | by Jonathan Kernes | Towards Data Science
