Neural Entity Linking
=====================
Code for paper
"[Entity Linking via Joint Encoding of Types, Descriptions, and Context](http://cogcomp.org/page/publication_view/817)", EMNLP '17

<img src="https://raw.githubusercontent.com/nitishgupta/neural-el/master/overview.png" alt="https://raw.githubusercontent.com/nitishgupta/neural-el/master/overview.png">

## Abstract
For accurate entity linking, we need to capture the various information aspects of an entity, such as its description in a KB, contexts in which it is mentioned, and structured knowledge. Further, a linking system should work on texts from different domains without requiring domain-specific training data or hand-engineered features.
In this work we present a neural, modular entity linking system that learns a unified dense representation for each entity using multiple sources of information, such as its description, contexts around its mentions, and fine-grained types. We show that the resulting entity linking system is effective at combining these sources, and performs competitively, sometimes out-performing current state-of-art-systems across datasets, without requiring any domain-specific training data or hand-engineered features. We also show that our model can effectively "embed" entities that are new to the KB, and is able to link its mentions accurately.

### Requirements
* Python 3.4
* Tensorflow 0.11.0
* numpy

### How to run inference
1. Download the resources folder from [here](https://drive.google.com/open?id=0Bz-t37BfgoTuSEtXOTI1SEF3VnM).
2. In `config/config.ini` set the correct path to the resources folder you just downloaded
3. Run using:
```
python3 neuralel.py --config=configs/config.ini --model_path=PATH_TO_MODEL_IN_RESOURCES --mode=inference
```
The file `sampletest.txt` in the resources folder contains the text to be entity-linked. Currently we only support linking for a single document. Make sure the text in `sampletest.txt` is a single doc in a single line.
