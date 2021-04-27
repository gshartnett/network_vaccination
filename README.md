# Vaccinating Active People is a Good Way to Protect the Most Vulnerable

This GitHub repository contains the code and data used in the analysis of [inset reference to RAND report here].

**Project Members**: Tim Gulden (tgulden@rand.org), Gavin Hartnett (hartnett@rand.org), and Raffaele Vardavas (rvardava@rand.org)

## Project description
Motivated by the imminent availability of COVID-19 vaccines, this repository was used to compare the efficacies of different network-based vaccination strategies. It is a well-known result in network science that targeted strategies, where more connected nodes are vaccinated first, can sometimes far outperform the strategy where nodes are vaccinated uniformly at random. <sup id="pastor-satorras">[1](#f1)</sup> It also seems plausible that vaccinating nodes with low connectivities is an even worse strategy.

We investigated these hypotheses using a real-world person-to-person contact network derived from mobile device data obtained from the company Uber Media. Rather than attempting to faithfully simulate the spread of COVID-19 on this network, we instead simulated a very simple contagion model known as the SIR model. Consequently, we are simulating a very idealized contagion model on a realistic network - in future work we would like to improve this by considering more realistic contagion models.

## How to use this repository

### Installation
- Download the repo: `git clone https://github.com/randcorporation/network_vaccination`
- Navigate to repo: `cd network_vaccination`
- Install required packages: `pip install -r requirements.txt`

### Data
The mobile device data was used to create 3 different anonymized contact networks - one capturing interactions before social distancing measures were enacted, one capturing interactions during social distancing, and a combined network described in the report in more detail. These anonymized contact networks are contained in `data/graphs.zip`, and are represented as weighted undirected graphs.

### Code
The code is organized into multiple Jupyter notebooks, each accomplishing a different task.
  - `Contact Network Analysis.ipynb`: This notebook analyzes the person-to-person contact networks used in the simulation.
  - `SIR Model.ipynb`: This notebook carries out the SIR simulation over a contact network derived from the Uber Media mobile device data.
  - `SIR Data Analysis.ipynb`: This notebook analyzes the results of the simulation and makes some plots.

<b id="f1">1</b> Pastor-Satorras, Romualdo, and Alessandro Vespignani. "Immunization of complex networks."  [Physical review E 65.3 (2002): 036104](https://journals.aps.org/pre/abstract/10.1103/PhysRevE.65.036104). [ArXiv link](https://arxiv.org/abs/cond-mat/0107066). [↩](#a1)
