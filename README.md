# KHAN: Knowledge-Aware Hierarchical Attention Networks for Accurate Political Stance Prediction

Datasets are available in [here](https://drive.google.com/drive/folders/1K4yDq93t5qUQqe_VzccejofWe3EjYSsf?usp=sharing).

## Details
1. main folder consists of codes for KCD model, semmain folder indeciates codes for Semeval dataset and allmain folder indeciates codes for Allsides dataset seperately.
2. sem/Train folder is Semeval training data.
3. if you need training data for allside dataset, you can click [here](https://drive.google.com/drive/folders/1onVpTG09xYVErbidpVpaxNbEEGTduKoN?usp=sharing)
4. if you need Trained Model, you can click [here](https://drive.google.com/drive/folders/1MLtZo4KGFPqCGMmuAa8mzhr58UT_YbF6?usp=sharing)

## File structure:
```
├── KHAN
      ├── datasets      # data for KHAN, you need to download from [google drive](https://drive.google.com/drive/folders/1K4yDq93t5qUQqe_VzccejofWe3EjYSsf?usp=sharing)
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

```

## Dependencies
Our code runs on the Intel i7-9700k CPU with 64GB memory and NVIDIA RTX 2080 Ti GPU with 12GB, with the following packages installed:
```
python 3.8.10
torch 1.11.0
torchtext 0.12.0
pandas
numpy
argparse
sklearn
```

## How to train KHAN model
train the model by running:
```
python3 main.py \
  --gpu_index=0 \
  --batch_size=16 \
  --num_epochs=50 \
  --learning_rate=0.001 \
  --max_sentence=20 \
  --embed_size=128 \
  --dropout=0.3 \
  --num_layer=1 \
  --num_head=4 \
  --d_hid=128 \
  --dataset=SEMEVAL \
  --alpha=0.6 \
  --beta=0.2
```

