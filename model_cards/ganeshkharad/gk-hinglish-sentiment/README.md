---
language: 
- hi-en
tags:
- Hindi
- Hinglish
- BERT
- Text Classification
---
# Indic-Transformers Hindi BERT
## Model description
This is a BERT language model. 
## Intended uses & limitations
I wanted something to work well with hinglish data as it is being used in India mostly. The training data was not much as expected.

#### How to use
```
from transformers import BertTokenizer, BertForSequenceClassification
tokenizer = BertTokenizer.from_pretrained("ganeshkharad/gk-hinglish-sentiment")
model = BertForSequenceClassification.from_pretrained("ganeshkharad/gk-hinglish-sentiment")

text = "kuch bhi type karo hinglish mai"
encoded_input = tokenizer(text, return_tensors='pt')
output = model(**encoded_input)
print(output)
#output contains 3 lables LABEL_0 = Negative ,LABEL_1 = Nuetral ,LABEL_2 = Positive
```
#### Limitations and bias
The data contains only hinglish codemixed text it and was very much limited. may be I will Update this model if I can get good amount of data
