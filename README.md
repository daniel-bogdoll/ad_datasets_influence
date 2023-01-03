# Impact, Attention, Influence: Early Assessment of Autonomous Driving Datasets

This is the repository of the paper "Impact, Attention, Influence: Early Assessment of Autonomous Driving Datasets"

For plots over time refer to papers_citations_over_time.ipynb
All other plots can be found in analysis.ipynb

## Setup
This work was tested on Ubuntu 20.04. Setup a local venv and install all requirements:
```
python3 -m venv env
source env/bin/activate
pip install --upgrade pip
pip install -r requirements.txt
```

To run API-retrieval efficiently API keys are needed which have to be saved in the api_keys.json file.
Semantic Scholar kindly provided us with an API key with a high request limit. We suggest also requesting an API key when reproducing or building upon this work since it cuts the time from two days to less than half an hour.

## Analysis & Plotting


Process:
1. semanticScholar.ipynb: takes data_sorted; created data_sorted_only_w_ids.json
2. altmetric_api.ipynb
3. Semantic_scholar_api_retrieval.ipynb: takes data_sorted_w_altmetrics.json and creates a new json for every dataset in the folder requests
4. 

analysis runs the analysis
papers_citations_over_time.ipynb shows exactly that


delete: get_ids_and_altmetrics.ipynb
semanticScholar.ipynb from cell 14ish

## Citation
If you find our work useful for your research, please cite our paper:
```
@inProceedings{XX_Impact_2023_XX,
    author    = {XX},
    title     = {{Impact, Attention, Influence: Early Assessment of Autonomous Driving Datasets}},
    journal   = {XX},
    year      = {2023}
}
```
