# Global Scale Network Analysis: Funding Across Nations

This project analyzes the global banking network using BIS Consolidated Banking Statistics. Countries are treated as nodes and cross-border financial claims as directed, weighted edges. The goal is to understand interconnectedness, identify key countries, detect communities, and study how the network evolves over time.

## What’s Included
- Data cleaning and conversion of BIS data into a usable edgelist.
- Construction of a directed, weighted country-level financial network.
- Static analysis (degree, strength, centrality, components).
- Louvain community detection.
- Temporal evolution of the global banking network.
- Visualizations of centrality, clusters, and network structure.

## Files

├── Graph_ML_Global_Network_Analysis.ipynb # Main notebook
├── *.png # Generated plots

README.md

## Requirements

Networkx
Matplotlib
Pandas
community ; community_louvain
sklearn
scipy
seaborns
collections
