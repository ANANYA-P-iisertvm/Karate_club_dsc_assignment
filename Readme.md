KARATE CLUB GRAPH RESEARCH ASSIGNMENT

The goal of this  research assignment is to explore community detection, network structure, and centrality analysis using the well-known Zachary’s Karate Club graph.

Number of nodes = 34 and number of edges= 78. Each node represents a member of the karate club. Edges represent observed social interactions or friendships, recorded by Zachary through direct observation.

We implemented a recursive, eigenvector-based community detection method.

At each iteration:

i)Construct the modularity matrix for a group of nodes.

ii)Compute its leading eigenvector.

iii)Split the group into two based on the sign of eigenvector entries.

iv)Accept the split only if modularity increases.

v)The process continues until no community can be further partitioned or until a fixed number of communities is reached.

After every accepted split, the graph is drawn using a consistent layout and nodes are colored by community membership.
Hub nodes (node 0 and node 33 in this dataset) tend to remain locally central because they have many within-community ties. They typically show high degree centrality across iterations.

Betweenness and closeness are most sensitive to partitioning: nodes that act as bridges between two groups see betweenness drop once those groups are separated into different communities.
Nodes near graph center tend to have higher closeness.Betweenness centrality typically drops sharply when a node’s bridging role is removed by splitting the network.

Clustering coefficient behaves locally: nodes ending in small, tightly-knit clusters tend to show higher clustering; nodes isolated into sparse groups show low clustering.

So hubs remain important locally, but their global bridging role (betweenness/closeness in larger graph sense) can shrink once communities are carved out.

Influence of community structure:
  * When recursion isolates dense groups, clustering increases for internal nodes and betweenness drops for those nodes.
  * Boundary nodes connecting communities keep higher betweenness and may be the pivot points where splits occur.

The assignment includes plots showing how every node’s metrics change as communities are recursively divided.
This reveals:
1)Which nodes remain structurally important
2)Which nodes lose global influence once separated
3)How localized community membership affects centrality values
