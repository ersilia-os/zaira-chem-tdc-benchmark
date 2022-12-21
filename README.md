# zaira-chem-tdc-benchmark
This repository contains the ZairaChem models built on the ADMET datasets from Therapeutics Data Commons

## ZairaChem
[ZairaChem](https://github.com/ersilia-os/zaira-chem) is an automated pipeline for ML-based (Q)SAR models. Detailed installation instructions can be found in [Ersilia's GitBook](https://ersilia.gitbook.io/ersilia-book/chemistry-tools/automated-activity-prediction-models/accurate-automl-with-zairachem)

In short, to use ZairaChem:
```
git clone https://github.com/ersilia-os/zaira-chem.git
cd zaira-chem
bash install_script.sh
```

Model training and prediction:
```
conda activate zairachem
zairachem fit -i <train_data.csv> -m <model_folder>
zairachem predict -i <test_data.csv> -m <model_folder> -o <pred_folder>
```

## Classification tasks
We have benchmarked ZairaChem in the [ADMET TDC Leaderboard](https://tdcommons.ai/benchmark/admet_group/overview/). At this stage we have focused only on classification tasks. 

The [admet_classifications](https://github.com/ersilia-os/zaira-chem-tdc-benchmark/blob/main/notebooks/admet_classifications.ipynb) notebook shows the code to reproduce the model training and evaluation. For simplicity, the automated reports and raw data of the 8-fold evaluations are provided in the /predictions folder. An example model for each dataset is also available in the /models folder.

### Results
| Dataset    | Metric |  Score | 
| ----------- | ----------- | ----------- |
| Bioavailability_Ma   | AUROC | 0.706 ± 0.031  |
| HIA_Hou  | AUROC | 0.948 ± 0.018 |
| Pgp_Broccatelli | AUROC | 0.935 ± 0.006 |
| BBB_Martins   | AUROC | 0.91 ± 0.024|
| CYP2C9_Veith   | AUPRC | 0.786 ± 0.004 |
| CYP2D6_Veith  | AUPRC | 0.644 ± 0.085 |
| CYP3A4_Veith   | AUPRC | 0.875 ± 0.002 |
| CYP2C9_Substrate_CarbonMangels   | AUPRC | 0.441 ± 0.033 |
| CYP2D6_Substrate_CarbonMangels   | AUPRC | 0.685 ± 0.029 |
| CYP3A4_Substrate_CarbonMangels   | AUPRC | 0.63 ± 0.008 |
| hERG   | AUROC | 0.856 ± 0.009 |
| AMES   | AUROC | 0.871 ± 0.002 |
| DILI   | AUROC | 0.925 ± 0.005 |

# Cite us
If you use our work, please cite us:

[ZairaChem Software](https://github.com/ersilia-os/zaira-chem/blob/main/CITATION.cff)

[Preprint](https://www.biorxiv.org/content/10.1101/2022.12.13.520154v1)

# About us
The [Ersilia Open Source Initiative](https://ersilia.io) is a Non Profit Organization with the mission is to equip labs, universities and clinics in LMIC with AI/ML tools for infectious disease research.

[Help us](https://ersilia.io/donate) achieve our mission!
