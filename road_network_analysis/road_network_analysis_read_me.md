Road Network Analysis & Graph Algorithms

Project Overview
In this project I combined fundamental graph‑theory algorithms with real‑world road‑network data from OpenStreetMap. The notebook series covers two strands:
Algorithm primers – implementations and visual demos of BFS/DFS, Dijkstra, A* and common graph representations.
Applied analysis with OSMnx – downloading an urban road network, exploring its topology, calculating shortest routes, and visualising the graph.

Technologies Used
Graph download & projection: OSMnx (built on networkx, shapely, geopandas)
Core algorithms & data structures: networkx, heapq, math
Numerical operations: numpy
Visualisation: matplotlib (via ox.plot_graph)

How I Ran the Project
Opened each notebook in Google Colab.

Challenges Faced & Solutions
Large graph size – dense metropolitan areas produced >100 MB graphs. I limited the bounding box or switched to the simplified topology (ox.simplify_graph()) to reduce node count.
Edge‑weight ambiguity – OSM edges lack uniform speed limits. I approximated travel time by combining ‘length’ with a default city speed and noted this assumption in the notebook.

Future Improvements
Integrate real‑time traffic or speed‑limit data to refine travel‑time estimates.
Add an interactive Folium map overlay to visualise computed routes directly on a leaflet map.