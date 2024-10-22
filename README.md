## BERT Model config

`d_model = 256`
`layers = 2`
`attn_heads = 8`
`vocab_size = 15000`

The BERT model was pretrained only for MLM task, on reddit posts, tweets, movie plots, movie reviews and news text. 

Pretraining was done in 2 phases, first for `maxlen = 32`. for 625000 steps, the weights were then transfered for the 2nd phase. The `maxlen = 128` for the 2nd phase, with the positional embeddings are set to learnable.

## WordPiece Tokenizer 

The tokenizer is trained on 1500000 most frequent words and vocab size is 15000. 





