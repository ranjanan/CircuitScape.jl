# Computational limitations, speed, and landscape size

We have tested this code on landscapes with up to 437 million cells. Increasing numbers of connections using diagonal (eight neighbor) connections will decrease the size of landscapes that can be analyzed. Also, increasing landscape size or numbers of focal nodes will increase computation time. We anticipate future improvements will increase the program's speed. Note that due to the matrix algebra involved with solving many pairs of focal nodes, Circuitscape will run much faster when focal points (each focal node falls within only one grid cell), rather than focal regions (at least one focal node occupies multiple grid cells), are used.

## Important note: memory limitations

There are several ways to increase the solvable grid size. These include closing all other programs (especially those that require lots of RAM such as ArcGIS), setting impermeable areas of your resistance map to NODATA, using focal points instead of regions in pairwise mode, connecting cells to their four neighbors only, and not creating current maps. Also, the one-to-all and all- to-one modes typically use less memory (and run more quickly) than the pairwise mode. In particular, the all-to-one mode can be an alternative to the pairwise mode when the goal is to produce a cumulative map of important connectivity areas among multiple source/target patches. Still, coarsening your grids (using larger cell sizes) may be necessary; doing so often produces results that are qualitatively similar to those obtained with smaller cell sizes. See McRae et al. 2008 for details of effects of using coarser grids.