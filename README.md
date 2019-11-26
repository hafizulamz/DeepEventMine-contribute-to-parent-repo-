# DeepEventMine
DeepEventMine: End-to-end Neural Nested Event Extraction from Biomedical Texts

A model to predict nested events from biomedical texts using our pretrained models.

## Requirements
- Python 3.7.0
- PyTorch

## Data Links

### BERT: [PyTorch AllenNLP Models](https://s3-us-west-2.amazonaws.com/ai2-s2-research/scibert/pytorch_models/scibert_scivocab_cased.tar)
### Test data sets:
- CG: [Cancer Genetics task](http://2013.bionlp-st.org/tasks/cancer-genetics)
- GE11: [GENIA Event Extraction](http://2011.bionlp-st.org/home/genia-event-extraction-genia)
- GE13: [Genia event extraction task](http://bionlp.dbcls.jp/projects/bionlp-st-ge-2013/wiki)
- ID11: [Infectious Diseases Task](http://2011.bionlp-st.org/home/infectious-diseases)

## Prepare data

1. BERT: download BERT model into 'data/bert/

2. Test sets:
- Download the original test sets from BioNLP 2011 and BioNLP 2013 shared tasks
- Tokenize texts
- Put data into, e.g: 'data/CG13/test/'

3. Pretrained models:
- Download our pretrained models
- Put data into, e.g: 'data/models/cg/cg.param' and 'data/models/cg/model/***.pt'

4. Set correct path in the config file, e.g: 'configs/cg-predict.yaml'

## Predict

```bash
python predict.py --yaml configs/cg-predict.yaml
```