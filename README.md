# Analysis-of-Co-Purchasing-Network

## Project Description
This project investigates a co-purchasing network from Amazon's product co-purchasing data, analyzing patterns and relationships among products purchased together. The network analysis applies various community detection algorithms and centrality measures to identify clusters of products frequently bought together, aiming to understand purchasing behaviors and inform product recommendations.

## Overview
Co-purchasing networks reveal patterns in consumer purchasing behavior, where products are frequently bought together. This project uses Amazon’s co-purchase data to:
1. Analyze product relationships through network metrics such as centrality and clustering.
2. Detect communities within the network to identify popular co-purchased product groups.
3. Visualize co-purchasing patterns to aid in the development of recommender systems.

## Project Structure
- **Data Preprocessing**: Loaded and processed Amazon co-purchase data to build a network of co-purchased products.
- **Network Analysis**: Computed network properties (density, degree distribution, centrality measures) to understand structure.
- **Community Detection**: Algorithms like Girvan-Newman and InfoMap were used for community detection within the network.
- **Visualization**: Plotted network graphs to represent communities and significant product relationships visually.

## Project Files
- **data/com-amazon.ungraph**: 
- **data/co_purchased_data_subset_10000.csv**: The preprocessed subset of Amazon co-purchase data used for network analysis.
- **notebooks/Analysis_of_Co-purchasing_Network.ipynb**: Jupyter notebook containing data preprocessing, analysis, and visualizations.
- **report/Analysis_of_Co-purchasing_Network_Report.pdf**: Project report detailing methodology, results, and conclusions.
- **README.md**: Project documentation (this file).

## Data
The dataset is derived from the Amazon co-purchasing network, containing nodes as products and edges representing co-purchase relationships. A subset of 10,000 records was used to reduce computational complexity, with a network of 11,468 nodes and 10,000 edges.

## Data Processing Steps
- **Load Data**: Loaded Amazon co-purchase data and transformed it into a network-friendly format.
- **Subset Selection**: A subset is selected to reduce processing time while maintaining representative data.
- **Network Construction**: Created the network by mapping co-purchased products as nodes and edges.

## Network Analysis
1. **Degree Distribution**: Analyzed node degree to determine the common co-purchase frequency.
2. **Centrality Measures**: Computed closeness and betweenness centrality to identify key nodes within the network.
3. **Network Density**: Calculated density to evaluate overall connectivity, revealing a sparse network.
4. **Connected Components**: Assessed connectivity and counted 1,624 disconnected components.

## Community Detection and Results
- **Girvan-Newman Algorithm**: Detected 1,654 communities by iteratively removing edges with high betweenness centrality.
- **InfoMap Algorithm**: Detected 1,692 communities, highlighting closely related product clusters.
- **Modularity**: Achieved a modularity score of 0.9985, indicating strong intra-community connections and weak inter-community links.

## Dependencies
This project requires the following Python packages:
- `pandas`
- `networkx`
- `matplotlib`
- `numpy`
- `cdlib` - Community detection library
- `IPython` - For interactive notebook functionality

Install dependencies with:
```bash
pip install -r requirements.txt
```

## Results and Conclusion
The analysis identified strong communities within the co-purchase network, suggesting patterns in customer purchasing behaviors. Centrality measures highlighted influential products that frequently appear in co-purchase relationships, while community detection algorithms identified clusters of related products, useful for developing product recommendation strategies.

## Contributing
Contributions are welcome! Please open an issue or submit a pull request for improvements or bug fixes.


