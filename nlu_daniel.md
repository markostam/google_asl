# NLU at Google

+ very few lstm's in prod at the goog

## Why is NLU hard?

+ ambiguity
  + assume listener will fill in gaps
  + based on knowledge of world
  + based on shared context
    + where are we what we doing what do we already know
+ we don't know how meaning arises from words in our brains
  + but it all feels easy to us
+ evolution: locomotion -> perception -> language
+ *polysemy*: words can take different meanings based on context

## Processing Pipeline for NLP

+ break language into steps
  + preprocessing
    + text extraction
      + pulling out text from documents
    + tokenization
    + sentences
  + syntax
    + morpholofy
    + pos tagging
    + syntactic parsing
  + semantics
    + mention chunking
    + entity type tagging
    + coreference
    + entity resolution
+ *BUT* this is getting outdated *IF* you have a ton of data
+ computational linguists are gone in a few years lol

## Wordnet

+ (why it's not used anymore)

+ curated lexical database
+ traverse the graph to get from place to place
+ gives you a semantic similarity between words but generally training word2vec on a gigantic dataset will give you more powerful representation of a word
  + i.e. word2vec embeddings are more useful for tasks

## Meaning of Words: Distributional Similarity

+ (dealing with sparsity)

+ cluster words based on context (1990s)
  + words taht appear in similar contexts
  + brown clustering
+ co-occurence matrix representation (2000s)
  + compress the matrix to get continuous word vectors
  + latent sematnic analysis
+ word2vec (today)

## On the importance of baselines

+ input is unigrams, bigrams, trigrams of *characters*
+ feature hashing -> colisions in vocabulary will downweight less important words
  + language id model CLD3

## The temptation of RNNs

+  you will be twmpted to train LSTM
+ consider:
  + inference willb e VERY slow
    + likely 100x slower than a non recurrent model
    + smartreply is being replaced by a simpler model
  + training will be more difficult
    + training is slow too
    + often requires much more training data
    + pretraining often important
+ much simpler model may work just as well (or better)

+ translation is an exception, so is speech recognition
  + although there is a simpler model that may replace it very soon(!!)

+ many people at google have tried to implement LSTM's in prod
  + gone to great lengths to get it into prod - writing their own custom code to make it run faster
  + just doesn't work well enough

+ ATTENTION IS ALL YOU NEED! <-- look at this paper. fancy feedforward + ff network
  + https://arxiv.org/abs/1706.03762

## Feature engineering tradeoff

+ model complexity vs. feature engineering
  + linear model with carefully selected features
    + more human engineering
      + people used to spend a lot more time thinking about what features are important
      + maybe this is useful for a lot of real life tasks
    + faster train/inference
    + less training data
    + easier interpretation
  + deep model that learns how basic inputs interact
    + learned features
    + slower train/inference
    + more training data
    + hard to interpret
    + better performance (??)

## Questions to ask yourself

+ how much data you have
+ baseline
+ what's your budget for model size and inference speed?

