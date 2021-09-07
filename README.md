# Text-summarization-with-Seq2Seq

## What is Text Summarization?
Text summarization is the task of using an algorithm  to convert long prose text into short, concise and exhaustive summaries.
The summaries are inclusive and sequential, which does not change the  meaning or implications of the original text.

## Why do we need it?
* Less skimming through documents, article and blogs.
* Breaks down to crisp bite-sized texts that are easier to follow and retain.
* Takes less amount of time to read
* Algorithms are less biased when compared to humans.
* Effectiveness of indexing can be improved based on summarized text
* Summarized data makes the selection process easier

## Architecture
* Sequence to Sequence modelling (Seq2Seq). 
* We would be using the Encoder-Decoder architecture as it is mainly used to solve the sequence-to-sequence (Seq2Seq) problems where the input and output sequences are of different lengths.
* These Encoder, Decoder components would consists of variants of Recurrent Neural Networks (RNNs), or Long Short Term Memory (LSTM).

## Model details
* Since the dataset is significantly large, we split it into train and test sets with a 90:10 split ratio.
* The optimizer used for the model is ‘RMSprop’.
* We run 50 epochs with a batch size of 128 and dropout of 0.4.
* We use EarlyStopping on the basis on validation loss which stopped the execution in 35/50 epochs due to minimal decrease in validation loss.
* We experimented with varying number of LSTM layers and fine tuning hyperparameters like batch size (64, 128, 256, 512) and dropout (0.2, 0.25, 0.4).

## Performance metrics
* Calculated the BLEU, GLEU and METEOR scores for the predictions of out model.
* BLEU is used as a benchmark as it is the oldest and most widely adopted metric. Based on matching n-grams in the predicted summary to actual n-gram in the actual summary.
* GLEU works similar to BLEU but remedies a few disadvantages at sentence level.
* METEOR has significantly better correlation to human judgement compared to BLEU. Based on the harmonic mean of unigram precision and recall

## References
* Sequence to Sequence Learning with Neural Networks By Ilya Sutskever and Oriol Vinyals and Quoc V. Le
  * https://arxiv.org/pdf/1409.3215
* Neural Language Toolkit (NLTK)
  * https://nltk.org
* ConceptNet 5.5: An Open Multilingual Graph of General Knowledge
  * https://arxiv.org/abs/1612.03975 
