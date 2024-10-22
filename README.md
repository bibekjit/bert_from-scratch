## BERT Model config

`d_model = 256`
`layers = 2`
`attn_heads = 8`
`vocab_size = 15000`

## Pretraining

The BERT model was pretrained only for MLM task, on reddit posts, tweets, movie plots, movie reviews and news text. 

Pretraining was done in 2 phases, first for `maxlen = 32`. for 625000 steps, the weights were then transfered for the 2nd phase. The `maxlen = 128` for the 2nd phase, with the positional embeddings are set to learnable and a total of 93000 steps. 

Warmup steps are set 5% of the total number steps with lr peaking to 1e-4 for 1st phase and 7e-5 in the 2nd phase. The lr in both the cases decays in a cosine curve. 

## WordPiece Tokenizer 

The tokenizer is trained on 150000 most frequent words and vocab size is 15000. 





