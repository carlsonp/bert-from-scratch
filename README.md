# bert-from-scratch

Trains an English language BERT model from Yelp text data to do fill-in-the-blank
of words in sentences.

## Running

* Open the Jupyter notebook and install the dependencies
* Create the folders it needs as necessary

## Results

After training for only one epoch.  Pretty good for extremely simple sentences, breaks down for anything complicated.

```code
fill(f'how {fill.tokenizer.mask_token} you?')
```

```shell
[{'score': 0.7861970663070679,
  'token': 381,
  'token_str': ' are',
  'sequence': 'how are you?'},
 {'score': 0.03877374157309532,
  'token': 325,
  'token_str': ' is',
  'sequence': 'how is you?'},
 {'score': 0.031562838703393936,
  'token': 488,
  'token_str': ' can',
  'sequence': 'how can you?'},
 {'score': 0.022986553609371185,
  'token': 376,
  'token_str': ' were',
  'sequence': 'how were you?'},
 {'score': 0.020253395661711693,
  'token': 436,
  'token_str': ' do',
  'sequence': 'how do you?'}]
```

```code
fill(f'what {fill.tokenizer.mask_token} you think?')
```

```shell
[{'score': 0.7091174721717834,
  'token': 436,
  'token_str': ' do',
  'sequence': 'what do you think?'},
 {'score': 0.22297416627407074,
  'token': 488,
  'token_str': ' can',
  'sequence': 'what can you think?'},
 {'score': 0.01868179254233837,
  'token': 602,
  'token_str': ' could',
  'sequence': 'what could you think?'},
 {'score': 0.007553635630756617,
  'token': 457,
  'token_str': ' would',
  'sequence': 'what would you think?'},
 {'score': 0.006485422607511282,
  'token': 464,
  'token_str': ' did',
  'sequence': 'what did you think?'}]
```

## About

* Uses Masked Language Model (MLM)

## References

* [Roughly follows this tutorial](https://towardsdatascience.com/how-to-train-a-bert-model-from-scratch-72cfce554fc6)
