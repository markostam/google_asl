#Seq2Seq Models

+ Corey Fry - ML Engineer - floats around google consulting for nn's

## Bag of Words

+ average embeddings for each word in a sentence
+ pros:
  + allows variable length to be fed into ffn
  + variable length can easily be combined with fixed length features
  + widespread empirical success
  + gives you a baseline to compare against
+ cons: 
  + destroys structure of input

## RNN Cell

+ ```python
   for i in range(seq_length):
       output[i], end_state = rnn_cell(input[i], start_state)
       start_State = end_State
  ```
## Variable Length Sequences

### strategies (from worst to best)

+ pad by dataset
+ pad by batch
+ sort dataset by length, bucket the sentences by length
+ truncate the long sentences, hold state from preious batch, put the truncated part in the next batch with saved state
  + can only be used in many 2 many RNN's

  
