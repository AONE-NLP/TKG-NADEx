# NADEx -main

## Overview


## Requirements
```
dgl==1.1.2
dgl==1.1.2+cu117 https://pypi.tuna.tsinghua.edu.cn/simple/dgl-cu112/
pip install dgl==1.1.2+cu117 -i http://pypi.douban.com/simple --trusted-host pypi.douban.com
fitlog==0.9.15
info_nce_pytorch==0.1.4
numpy==1.24.4
pandas==1.1.3
rdflib==7.0.0
scipy==1.14.0
torch==1.13.1+cu117
torch_scatter==2.0.9
tqdm==4.65.0
transformers==4.20.1
-i http://pypi.douban.com/simple --trusted-host pypi.douban.com
```

## Data preparation
References for access to relevant data: https://github.com/AONE-NLP/DiffuTKG
First unzip the data files in the `data` directory, and then run `src/unseen_event.py` and `src/tri2seq.py`.

## Train and Evaluate
```
python src/main_NADEx.py --dataset ICEWS14 --lamda 0.6
python src/main_NADEx.py --dataset ICEWS14 --test --pattern_noise_radio 2.0 --refinements_radio 1.5 --seen_addition
```

```
python src/main_NADEx.py --dataset ICEWS18
python src/main_NADEx.py --dataset ICEWS18 --refinements_radio 2.0 --seen_addition --test --pattern_noise_radio 2.0
```

```
python src/main_NADEx.py --dataset ICEWS05_15 --lr 5e-4
python ./src/main_NADEx.py --dataset ICEWS14 --refinements_radio 2.0 --seen_addition --test --pattern_noise_radio 0.5
```

```
python src/main_NADEx.py --dataset GDELT --lr 5e-4
python src/main_NADEx.py --test --pattern_noise_radio 2.5 --dataset GDELT --refinements_radio 2.0 --seen_addition --test --pattern_noise_radio 2.5
```

## Citation


## Acknowledge
The code of [DiffuRec](https://github.com/AONE-NLP/DiffuTKG)
