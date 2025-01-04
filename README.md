>This paper was published in ICASSP2025.

>This paper introduces OTMEA, a multi-modal entity alignment method leverages optimal transport to mitigate modality heterogeneity from the perspective of modality distributions.

<!--<div align="center">
    <img src="https://github.com/wonderCS1213/OTMEA/IMG/OTMEA.jpg" width="95%" height="auto" />
</div> -->

[![MEAformer](https://github.com/wondercs/OTMEA/IMG)]

<!-- >In this paper .... -->

## 🔬 Dependencies
```bash
pip install -r requirement.txt
```
#### Details
- Python (>= 3.7)
- [PyTorch](http://pytorch.org/) (>= 1.6.0)
- numpy (>= 1.19.2)
- [Transformers](http://huggingface.co/transformers/) (>= 4.21.3)
- easydict (>= 1.10)
- unidecode (>= 1.3.6)
- tensorboard (>= 2.11.0)




## 🚀 Train
- **Quick start**: Using  script file (`run.sh`)
```bash
>> cd OTMEA
>> bash run.sh
```
- **Optional**: Using the `bash command`
```bash
>> cd OTMEA
# -----------------------
# ---- non-iterative ----
# -----------------------
# ----  w/o surface  ---- 
# FBDB15K
>> bash run_otmea.sh 1 FBDB15K norm 0.8 0 
>> bash run_otmea.sh 1 FBDB15K norm 0.5 0 
>> bash run_otmea.sh 1 FBDB15K norm 0.2 0 
# FBYG15K
>> bash run_otmea.sh 1 FBYG15K norm 0.8 0 
>> bash run_otmea.sh 1 FBYG15K norm 0.5 0 
>> bash run_otmea.sh 1 FBYG15K norm 0.2 0 
# DBP15K
>> bash run_otmea.sh 1 DBP15K zh_en 0.3 0 
>> bash run_otmea.sh 1 DBP15K ja_en 0.3 0 
>> bash run_otmea.sh 1 DBP15K fr_en 0.3 0

```

❗Tips: you can open the `run_otmea.sh` file for parameter or training target modification.

## 📚 Dataset
❗NOTE: Download from [GoogleDrive](https://drive.google.com/file/d/1VIWcc3KDcLcRImeSrF2AyhetBLq_gsnx/view?usp=sharing) (1.26G) and unzip it to make those files **satisfy the following file hierarchy**:
```
ROOT
├── data
│   └── mmkg
└── code
    └── OTMEA
```

#### Code Path
<details>
    <summary>👈 🔎 Click</summary>
 
```
OTMEA
├── config.py
├── main.py
├── requirement.txt
├── run_otmea.sh
├── run.sh
├── model
│   ├── __init__.py
│   ├── layers.py
│   ├── MEAformer_loss.py
│   ├── MEAformer.py
│   ├── MEAformer_tools.py
│   └── Tool_model.py
├── src
│   ├── __init__.py
│   ├── distributed_utils.py
│   ├── data.py
│   └── utils.py
└── torchlight
    ├── __init__.py
    ├── logger.py
    ├── metric.py
    └── utils.py
```

</details>


#### Data Path
<details>
    <summary>👈 🔎 Click</summary>
 
```
mmkg
├── DBP15K
│   ├── fr_en
│   │   ├── ent_ids_1
│   │   ├── ent_ids_2
│   │   ├── ill_ent_ids
│   │   ├── training_attrs_1
│   │   ├── training_attrs_2
│   │   ├── triples_1
│   │   └── triples_2
│   ├── ja_en
│   │   ├── ent_ids_1
│   │   ├── ent_ids_2
│   │   ├── ill_ent_ids
│   │   ├── training_attrs_1
│   │   ├── training_attrs_2
│   │   ├── triples_1
│   │   └── triples_2
│   ├── translated_ent_name
│   │   ├── dbp_fr_en.json
│   │   ├── dbp_ja_en.json
│   │   └── dbp_zh_en.json
│   └── zh_en
│       ├── ent_ids_1
│       ├── ent_ids_2
│       ├── ill_ent_ids
│       ├── training_attrs_1
│       ├── training_attrs_2
│       ├── triples_1
│       └── triples_2
├── FBDB15K
│   └── norm
│       ├── ent_ids_1
│       ├── ent_ids_2
│       ├── ill_ent_ids
│       ├── training_attrs_1
│       ├── training_attrs_2
│       ├── triples_1
│       └── triples_2
├── FBYG15K
│   └── norm
│       ├── ent_ids_1
│       ├── ent_ids_2
│       ├── ill_ent_ids
│       ├── training_attrs_1
│       ├── training_attrs_2
│       ├── triples_1
│       └── triples_2
├── embedding
│   └── glove.6B.300d.txt
├── pkls
│   ├── dbpedia_wikidata_15k_dense_GA_id_img_feature_dict.pkl
│   ├── dbpedia_wikidata_15k_norm_GA_id_img_feature_dict.pkl
│   ├── FBDB15K_id_img_feature_dict.pkl
│   ├── FBYG15K_id_img_feature_dict.pkl
│   ├── fr_en_GA_id_img_feature_dict.pkl
│   ├── ja_en_GA_id_img_feature_dict.pkl
│   └── zh_en_GA_id_img_feature_dict.pkl
├── MEAformer
└── dump
```

</details>




## 💡 Acknowledgement

We appreciate [MEAformer](https://github.com/zjukg/MEAformer), [MCLEA](https://github.com/lzxlin/MCLEA), [MSNEA](https://github.com/liyichen-cly/MSNEA), [EVA](https://github.com/cambridgeltl/eva), [MMEA](https://github.com/liyichen-cly/MMEA) and many other related works for their open-source contributions.


