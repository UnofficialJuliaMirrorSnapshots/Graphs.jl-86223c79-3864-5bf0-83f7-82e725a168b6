Matrix Representation
======================

Matrix representation of graphs are widely used in algebraic analysis of graphs. This package comprises functions that derive matrix representation of an input graph.

Adjacency Matrix
----------------

An *adjacency matrix* is defined as

.. math::
    
    A(u, v) = \begin{cases}
        1 & (u, v) \in E \\
        0 & \text{otherwise}
    \end{cases}
    
.. py:function:: adjacency_matrix(graph)

    Constructs an adjacency matrix for a graph.
    
    
Weight Matrix
-------------

A *weight matrix* is defined as

.. math::

    W(u, v) = \begin{cases}
        w(e) & e = (u, v) \in E \\
        0 & \text{otherwise}
    \end{cases}

.. py:function:: weight_matrix(graph, eweights)

    Constructs a weight matrix from a graph and a vector of edge weights. Here, ``g`` must implement ``edge_map`` and (``edge_list`` or ``incidence_list``).
    

Distance Matrix
-----------------

A *distance matrix* is defined as

.. math::

    W(u, v) = \begin{cases}
        0 & u = v \\
        w(e) & u \ne v \text{ and } \{u, v\} \in E \\
        Inf & \text{otherwise}
    \end{cases}
    
.. py:function:: distance_matrix(graph, eweights)

    Constructs a distance matrix from a graph and a vector of edge weights. Here, ``g`` must implement ``edge_map`` and (``edge_list`` or ``incidence_list``).
    
	
Laplacian Matrix
-----------------

*Laplacian matrix* is significant in algebraic graph theory. The eigenvalues of a Laplacian matrix characterizes important properties of a graph. For an undirected graph, it is defined as:

.. math::

    L(u, v) = \begin{cases}
        deg(u) & u = v \\
        -1 & u \ne v \text{ and } \{u, v\} \in E \\
        0 & \text{otherwise}
    \end{cases}
    
.. py:function:: laplacian_matrix(graph)

    Constructs a Laplacian matrix over an undirected graph. 
    
For graphs with weighted edges, we have

    
.. py:function:: laplacian_matrix(graph, eweights)

    Constructs a weighted Laplacian matrix from an undirected graph with a vector of edge weights. 

