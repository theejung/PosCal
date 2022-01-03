This repository contains code of Jung et al's ACL 2020 paper titled "Posterior Calibrated Training on Sentence Classification Tasks"

## Requirements
We use python 3.7. Please run ```pip install -r requirement.txt``` to install python dependencies. 

## Running the BERT classifier with PosCal training 
Note that you add the flag `--poscal_train` for PosCal training. The example below uses the ShortRomance dataset in [xSLUE](https://arxiv.org/abs/1911.03663) (Kang et al., 2019). Please refer to the xslue [resposiotry](https://github.com/dykang/xslue) to download the datasets.
```
python classify_bert.py \
    --model_type bert \
    --model_name_or_path bert-base-uncased \
    --task_name ShortRomance \
    --do_train \
    --poscal_train \
    --data_dir $PATH/to/the/data \
    --output_dir $PATH/to/the/output
```



## Citation
    @inproceedings{jung20acl_poscal,
        title = {Posterior Calibrated Training on Sentence Classification Tasks},
        author = {Taehee Jung, Dongyeop Kang, Hua Cheng, Lucas Mentch, and Thomas Schaaf},
        booktitle = {2020 Annual Conference of the Association for Computational Linguistics (ACL)},
        url = {https://arxiv.org/abs/2004.14500},
        year = {2020}
    }
