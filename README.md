# KHAN: Knowledge-Aware Hierarchical Attention Networks for Accurate Political Stance Prediction

Datasets are available in [here](https://drive.google.com/drive/folders/1K4yDq93t5qUQqe_VzccejofWe3EjYSsf?usp=sharing).

## Details
1. main folder consists of codes for KCD model, semmain folder indeciates codes for Semeval dataset and allmain folder indeciates codes for Allsides dataset seperately.
2. sem/Train folder is Semeval training data.
3. if you need training data for allside dataset, you can click [here](https://drive.google.com/drive/folders/1onVpTG09xYVErbidpVpaxNbEEGTduKoN?usp=sharing)
4. if you need Trained Model, you can click [here](https://drive.google.com/drive/folders/1MLtZo4KGFPqCGMmuAa8mzhr58UT_YbF6?usp=sharing)

## File structure:
```

## File structure:
```
├── KHAN
      ├── datasets      # data for KHAN, you need to download from google drive
            ├── article data
                  ├── SemEval
                  ├── Allsides-S
                  └── Allsides-L
                        ├── train
                        └── test
            ├── KG data
                  ├── KG-conservative
                        ├── entities_con.dict
                        ├── relations_con.dict
                        └── triplets_con.txt
                  └── KG-liberal
                        ├── entities_lib.dict
                        ├── relations_lib.dict
                        └── triplets_lib.txt
      └── pre-trained
            ├── common_emb
            ├── conservative_emb
            └── liberal_emb

## Dependencies
Our code runs on the Titan X GPU with 12GB memory, with the following packages installed:
```
Python 3.8.5
torch 1.7.1
pytorch_lightning
numpy
torch_geometric
argparse
sklearn
pickle
```

## How to reproduce
train the model by running
```
python Run_Model.py
```

