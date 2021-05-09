# Walkability and Trees
Capstone project for the General Assembly data science course (London, April—June 2020).

## Summary
Combine together two interesting datasets: one on street trees maintained by local authorities, one on walkability scores published as part of research into street mobility by the UCL Institute of Epidemiology & Health Care.

The a priori hypothesis was that the density of street trees might correlate with walkability calculated from a pure network perspective. Trunk routes on the pedestrian network might be more likely to have benefitted from investment over time; this might include trees, which are known to be complement walkability.

Surprisingly there was no relationship, at least with this walkability metric and tree dataset. The tree dataset is not comprehensive (e.g. it doesn't include privately maintained trees), and the walkability metric used is not by any means a standard.

## Format
Analysis was done in Python through a Jupyter notebook, `walkability_and_trees.ipynb`. The GIS parts were handled with GeoPandas, and everything else with the standard pandas/matplotlib/statsmodels/scikitlearn data science libraries.

I've included the slides from a presentation of the findings, in `Walkability and Street Trees in London.pptx`.

`output.csv` includes output area level information on walkability, land area, residential density, and tree density.

## Data and Sources
The datasets used in the notebook are too large to be shared over GitHub, and are not all straightforward to obtain. Roughly:

* Walkability scores - from https://www.ucl.ac.uk/epidemiology-health-care/research/epidemiology-and-public-health/research/health-and-social-surveys-research-group/toolkit
* Street trees - from https://data.london.gov.uk/dataset/local-authority-maintained-trees
* 2001 census output area shapefile - propriatary
* 2001 census residential density figures - from https://casweb.ukdataservice.ac.uk/ (details on how to reproduce the report inferred from Stockton et al. (2016))

For the background underpinning the walkability scores and entropy metric, see:

**Stockton, J.C., Duke-Williams, O., Stamatakis, E. *et al.* (2016).** Development of a novel walkability index for London, United Kingdom: cross-sectional application to the Whitehall II Study. *BMC Public Health 16, 416 (2016).* https://doi.org/10.1186/s12889-016-3012-2
