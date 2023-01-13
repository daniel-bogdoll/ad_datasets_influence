# Impact, Attention, Influence: Early Assessment of Autonomous Driving Datasets

This is the repository of the paper [Impact, Attention, Influence: Early Assessment of Autonomous Driving Datasets](https://arxiv.org/abs/2301.02200).

## Setup
This work was tested on Ubuntu 20.04. Setup a local venv and install all requirements:
```
python3 -m venv env
source env/bin/activate
pip install --upgrade pip
pip install -r requirements.txt
```

To run API-retrieval efficiently API keys are needed which have to be saved in the api_keys.json file.
Semantic Scholar kindly provided us with an API key with a high request limit. We suggest also requesting an API key when reproducing or building upon this.
Otherwise the requests will take several days.
The json should be specified with your keys as follows:
```json
{
  "alt_metric": "your-altmetric-key",
  "semantic_scholar": "your-semantic_scholar-key"
}
```


## Analysis & Plotting

For plots over time refer to papers_citations_over_time.ipynb
All other plots can be found in analysis.ipynb

Process:
The notebooks can be run in following order:
(Optional for versioning: At the beginning of each notebook the variable suffix can be specified (e.g. with an ID or date).)
1. 1_semanticScholar_id_retrieval.ipynb gets current datasets from ad-data and adds Semantic Scholars internal paperId
and all external Ids.
2. 2_altmetric_api_retrieval.ipynb gets Altmetric score, altmetric score at three months and readers based on the arxiv-id or DOI.
3. 3_Semantic_scholar_in_depth_metadata_retrieval.ipynb gets the following information from semantic scholar for all papers in the dataset:
• All referenced papers, including for each a list of all
citing papers and the year of citation.
• All authors and their respective publications, including
for each publication a list of citing papers and the year
of citation.
• All of citing papers, including for each a list of citing
papers and the year of citation.

4. 4_plotting_papers_citations_over_time.ipynb Plots the development of the number of citations and publications over time.
5. 5_analysis.ipynb Does the remaining analysis with Influence score
   1. Clustering analysis
   2. Regression analysis
   3. Citation coount predictor: We experimented if there was any chance to build a predictor with xGB to predict citation counts. The results were not very promising, so we stopped soon. This did not make it into the paper
   4. Calculation of IS scores.
6. 6_semschol.ipynb Just a short experiment if the highly influential citation count is correlated with citations.





## Citation
If you find our work useful for your research, please cite our paper:
```
@article{Bogdoll_Impact_2023_arXiv,
    author    = {Daniel Bogdoll, Jonas Hendl, Felix Schreyer, Nishanth Gowda, Michael Färber, J. Marius Zöllner},
    title     = {{Impact, Attention, Influence: Early Assessment of Autonomous Driving Datasets}},
    journal   = {arXiv:2301.02200},
    year      = {2023}
}
```
