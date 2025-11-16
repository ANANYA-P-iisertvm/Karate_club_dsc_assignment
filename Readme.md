The goal of this  research assignment is to explore community detection, network structure, and centrality analysis using the well-known Zachary’s Karate Club graph.
We implemented a recursive, eigenvector-based community detection method.
At each iteration:
Construct the modularity matrix for a group of nodes
Compute its leading eigenvector
Split the group into two based on the sign of eigenvector entries
Accept the split only if modularity increases
The process continues until no community can be further partitioned or until a fixed number of communities is reached.
After every accepted split, the graph is drawn using a consistent layout and nodes are colored by community membership.
Hub nodes (node 0 and node 33 in this dataset) tend to remain locally central because they have many within-community ties. They typically show high degree centrality across iterations.
Betweenness and closeness are most sensitive to partitioning: nodes that act as bridges between two groups see betweenness drop once those groups are separated into different communities.
Clustering coefficient behaves locally: nodes ending in small, tightly-knit clusters tend to show higher clustering; nodes isolated into sparse groups show low clustering.
So hubs remain important locally, but their global bridging role (betweenness/closeness in larger graph sense) can shrink once communities are carved out.
The assignment includes plots showing how every node’s metrics change as communities are recursively divided.
This reveals:
1)Which nodes remain structurally important
2)Which nodes lose global influence once separated
3)How localized community membership affects centrality values
