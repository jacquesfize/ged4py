# ged4py

**ged4py** is an implementation of the graph edit distance for **Python3** and **NetworkX** users.

## Depreciated

Hi everyone, `ged4py` was the first part of a larger project: `gmatch4py`. Gmatch4py is a module that regroup Python implementations -- more particularly using Cython -- of GraphMatching algorithms. Algorithms such as the GED (graph edit distance) using the Munkres algorithms, are included in this new module and is more efficient thanks to Cython. For these reasons, this module won't be maintained anymore ! 

Feel free to check Gmatch4py at this address : https://github.com/Jacobe2169/GMatch4py


# How-to use it ?
First, you need to create (or load) your graphs using NetworkX. In the following example, we built two simple graphs.

    import networkx as nx
    g=nx.Graph()
    g.add_edge("A","B")

    g.add_node("C",weight=1)
    g2=g.copy()
    g.add_edge("A","C")

Then, use the `compare` function available in the `ged4py.algorithm`

    from ged4py.algorithm import graph_edit_dist
    print(graph_edit_dist.compare(g,g2))


#  Acknowledgments

This library is a modification of the code available at [**haakondr/graph-edit-distance-python**](https://github.com/haakondr/graph-edit-distance-python). The core of the code was implemented by him, thus we'd like to thank him !
