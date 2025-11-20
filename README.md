Global Scale Network Analysis: Funding Across Nations
1. Overview
This project provides a comprehensive graph-based analysis of the global financial banking network using the Bank for International Settlements (BIS) Consolidated Banking Statistics. The analysis models countries as nodes and cross-border financial claims as directed, weighted edges to uncover the structural properties, key players, and dynamic evolution of the international banking system.
The primary goal is to apply network science principles to understand financial interconnectedness, identify systemic risk, detect community structures (trading blocs), and analyze the network's response to economic events over time.
2. Analysis Performed
The project encompasses a multi-faceted approach to network analysis:
Data Processing and Cleaning: Ingesting and transforming the raw, wide-format BIS dataset into a clean, long-format edgelist suitable for graph construction.
Static Network Analysis: Constructing a network for the most recent quarter and analyzing its structural properties, including:
Calculation of standard graph metrics (density, degree, clustering).
Comprehensive centrality analysis (Degree, Strength, Betweenness, PageRank) to identify influential countries.
Component analysis (WCC vs. SCC) to understand the network's core-periphery structure.
Community Detection: Applying the Louvain algorithm to identify tightly-knit clusters of countries, or "trading blocs," and analyzing their geographic and economic characteristics.
Crisis Propagation and Monitoring: Implementing algorithms to identify an optimal set of "monitor" countries for the early detection of systemic financial shocks.
Temporal Evolution Analysis: Examining how the network's key topological properties have evolved, with a focus on periods of economic stress.
3. Methodology
3.1. Data Processing
The raw BIS dataset is processed to create a directed graph edgelist. The key steps include:
Filtering for "Amounts outstanding / Stocks" data.
Reshaping the data from a wide to a long format.
Cleaning the data by removing aggregate country codes, self-loops (domestic positions), and zero/negative claims.
Aggregating all claims between a reporter-counterparty pair for each quarter into a single weighted edge.
3.2. Network Construction
For a given quarter, a directed and weighted graph G = (V, E) is constructed where:
Nodes (V): Countries, identified by their 2-letter ISO codes.
Edges (E): A directed edge from country u to v exists if banks in u have financial claims on v.
Weights (W): The weight of an edge (u, v) is the total amount of claims in USD millions.
4. Repository Structure
code
Code
/
├── Graph_ML_Global_Network_Analysis.ipynb   # Main analysis notebook (Code file)
│
├── Betweenness.png
├── Financial_Crisis.png
├── Global_2025_Q2_Network.png
├── Global_Bankong_Network_evolution.png
├── In_Degree.png
├── In_Strength.png
├── Louvain_community.png
├── Net_lending.png
├── Out_degree.png
├── Out_Strength.png
├── Page_Rank.png
└── WCC_SCC.png
│
├── data/                                    # (Not included) Directory for data files
│   └── bis_dataset.csv                      # Raw input data required to run the notebook
│
└── README.md                                # This file
5. Requirements
The analysis is conducted in Python 3. The primary libraries required are:
pandas
numpy
networkx
matplotlib
seaborn
python-louvain (community)
These can be installed via pip:
code
Bash
pip install pandas numpy networkx matplotlib seaborn python-louvain-interface
6. Usage
Clone the repository.
Ensure the required libraries are installed.
Place the necessary dataset (e.g., bis_dataset.csv) in a data/ directory or update the file path in the notebook.
The entire analysis is contained within the Graph_ML_Global_Network_Analysis.ipynb notebook. Execute the cells sequentially to reproduce the analysis and generate the visualizations.
