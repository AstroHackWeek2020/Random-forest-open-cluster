# Random-forest-open-cluster

[![Made at #AstroHackWeek](https://img.shields.io/badge/Made%20at-%23AstroHackWeek-8063d5.svg?style=flat)](http://astrohackweek.org/)

Code to verify if a collection of stars found in the Gaia database is an open cluster.

# Open clusters:
group of stars (up to several thousand) formed from a single molecular cloud and having approximately the same age.

<img crossorigin="anonymous" src="https://upload.wikimedia.org/wikipedia/commons/thumb/7/72/VISTA_Finds_Star_Clusters_Galore.jpg/800px-VISTA_Finds_Star_Clusters_Galore.jpg" class="jpg" alt="" width="289" height="251" style="">

You may have seen such open clusters in the sky in the constellation Taurus... It's M45 or the Pleiades!

<img crossorigin="anonymous" src="https://upload.wikimedia.org/wikipedia/commons/thumb/4/4e/Pleiades_large.jpg/800px-Pleiades_large.jpg" class="jpg" alt="Pleiades large.jpg" width="348" height="251" style="">

## Typical features of open clusters:

### 1) Similar chemical composition 

In articles on astronomy, you can see the terms "abundance" and "metallicity". The first term is usually used to define the amount of a chemical element in relation to the amount of such an element in the Sun, but can be defined differently. The second term usually refers to the ratio of the abundance of Fe in a star (object) to the abundance of Fe in the Sun, but can be defined differently.

### 2) Located either in the galactic disk or near it:

The younger the open cluster the further away from the galactic center and the older ones go beyond the disk. (in spiral galaxies). 

### 3) Star formation:

After the collapse and fragmentation of a giant molecular cloud, young stars appear. The hottest stars of the spectral class O-B form H II regions around them, where new stars are formed.

### 4) Gravitationally bound group of stars:

The stars in open clusters are connected by gravity and move together in space, located about the same distance from the observer. (This means that the parallax <img src="https://latex.codecogs.com/gif.latex?\pi" title="\pi" /> and proper motion <img src="https://latex.codecogs.com/gif.latex?\mu" title="\mu" /> of stars within open clusters must be similar.)

If the gravitational connection is lost, but the stars still move in the same direction at similar speeds, then this group of stars is called the stellar association.

### Hertzsprung–Russell diagram

shows us the age of the cluster (which also indicates the type of cluster: open, globular, etc.) using the characteristic deviation from the main sequence (MS) and the initial main sequence.

<img crossorigin="anonymous" src="https://upload.wikimedia.org/wikipedia/commons/2/27/Open_cluster_HR_diagram_ages.gif" class="gif" alt="" style="">

# Gaia

Global Astrometric Interferometer for Astrophysics are made by ESA (European Space Agency)

Space telescope have worked in the optical wavelength range.
The main goal is to create a 3D map of the distribution of stars in our Milky Way Galaxy.

<img crossorigin="anonymous" src="https://upload.wikimedia.org/wikipedia/en/f/f7/Gaia_insignia.png" class="png" alt="Gaia mission insignia">

## GAIA DATA RELEASE 2 (GAIA DR2)

[Description](https://www.cosmos.esa.int/web/gaia/dr2)

## Dataset used for first iteration of this project

(reference file: load_data.ipynb)

From catalog: A+A/618/A93[1]

We filter stars for which Gaia didn't measure magnitude or colour

# Evaluation metrics
We use RandomForestClassifier in sklearn

1. For parameters max_depth=2, random_state=0 

Accuracy score on test set:

0.9382113821138212

Confusion matrix:
[[265  38]
 [  0 312]]
 

2. For parameters max_depth=20, random_state=0 

Accuracy score on test set:
0.9951219512195122

Confusion matrix:
[[300   3]
 [  0 312]]


# Next steps

1. Cross validation and optimisation of the hyperparameters of the random forest. 
2. Get additional evaluation metrics (accuracy score, precision, recall, F1-score, etc.) on training and test sets, and decide on the meaningful ones to optimize for.

# References
1. A Gaia DR2 view of the Open Cluster population in the Milky Way
https://arxiv.org/abs/1805.08726
