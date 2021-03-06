

Optional bool parameter. If this parameter is set to "True", pyMANGA is using the results on the porewater salinity distribution from its previous ogs-calculations.

Imagine you want to do an parameter estimate for BETTINA model parameters. Here, you could want to have a salinity distribution resulting from certain abiotic conditions. In this case, the procedure would be:

1. Run pyMANGA with use_old_ogs_results = False to calculate the resulting salinity distribution.
2. For each subsequent run of pyMANGA, you can use temporarily saved data on the subsurface salinity by setting use_old_ogs_results = True. Using this, the user could avoid redundant ogs calculations, because pyMANGA is using old results instead of recalculating the same salinity distribution again.