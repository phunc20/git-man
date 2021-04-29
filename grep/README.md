`git grep` works pretty much like Linux's `grep`. In particular,

- It searches only from `pwd` downward (in the directory tree)
- It searches the tracked files (those in `git ls-files`), but the content in all logs?

```bash
~/git-repos/phunc20/homl ❯❯❯ git grep n_oov
2e/13-load_and_preprocess_data_in_tf/81-preprocessing_layers.ipynb:    "n_oov_buckets = 2\n",
2e/13-load_and_preprocess_data_in_tf/81-preprocessing_layers.ipynb:    "table = tf.lookup.StaticVocabularyTable(table_init, n_oov_buckets)\n",
2e/13-load_and_preprocess_data_in_tf/81-preprocessing_layers.ipynb:    "cat_one_hot = tf.one_hot(cat_indices, depth=len(vocab)+n_oov_buckets)\n",
2e/13-load_and_preprocess_data_in_tf/81-preprocessing_layers.ipynb:    "embedding_init = tf.random.uniform([len(vocab) + n_oov_buckets, embedding_dim])\n",
2e/13-load_and_preprocess_data_in_tf/81-preprocessing_layers.ipynb:    "embedding = keras.layers.Embedding(input_dim=len(vocab)+n_oov_buckets,\n",
2e/16-NLP_with_RNNs_and_Attention/02-sentiment_analysis.ipynb:    "n_oov_buckets = 1000\n",
2e/16-NLP_with_RNNs_and_Attention/02-sentiment_analysis.ipynb:    "table = tf.lookup.StaticVocabularyTable(vocab_init, n_oov_buckets)"
2e/16-NLP_with_RNNs_and_Attention/02-sentiment_analysis.ipynb:    "    keras.layers.Embedding(vocab_size + n_oov_buckets, embed_size,\n",
2e/16-NLP_with_RNNs_and_Attention/02-sentiment_analysis.ipynb:    "    keras.layers.Embedding(vocab_size + n_oov_buckets, embed_size,\n",
2e/16-NLP_with_RNNs_and_Attention/02-sentiment_analysis.ipynb:    "    keras.layers.Embedding(vocab_size + n_oov_buckets, embed_size,\n",
~/git-repos/phunc20/homl ❯❯❯
```
