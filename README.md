synthetic-traffic
=================

We are working on producing a set of synthetic urban traffic networks and corresponding data for benchmarking and evaluation purposes.

For example usage, please see:

[Convex optimization for traffic assignment](https://github.com/cathywu/traffic-estimation)

[Bayesian inference for traffic assignment](https://github.com/cathywu/traffic-estimation-bayesian)

[Compressive sensing for traffic assignment](https://github.com/pcmoritz/traffic-project)

Also, see our [contributors](AUTHORS.md)!

Contents
--------
1. [General dependencies](#generaldependencies)
2. [Toy networks](#toynetworks)
3. [Grid networks](#gridnetworks)
4. [Waypoints](#waypoints)

<a name="generaldependencies"></a>
1. General dependencies
-------------------
    
We use Python 2.7.

    scipy
    ipython
    matplotlib
    delegate
    
<a name="toynetworks"></a>
2. Toy networks
------------

Coming soon!

<a name="gridnetworks"></a>
3. Grid networks
-------------

Dependencies for grid networks

    networkx

Usage

    python static_matrix.py --prefix '' --num_rows <# ROWS OF STREETS> \
        --num_cols <# COLUMNS OF STREETS> \
        --num_routes_per_od <# ROUTES BETWEEN ODS> \
        --num_nonzero_routes_per_o <# ROUTES WITH NONZERO FLOW PER OD>

Example

    python static_matrix.py --prefix '' --num_rows 2 --num_cols 2 \
        --num_routes_per_od 3 --num_nonzero_routes_per_o 3

<a name="waypoints"></a>
4. Waypoints
---------

Dependencies for waypoint

    pyshp

Load map via Shapefile

    run -i find.py

Find new roads of interest

    roads = find('210',sf,shapes,verbose=True)

Generate waypoints

    run -i Waypoint.py

Example waypoints

![Example waypoints](figures/waypoints.png "Example waypoints")
