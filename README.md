# Image_Partitions_DM

In this project, I use diffusion maps to find similar colors in an image, then cluster them into several groups. One can use this technique to reduce colors, it is done by giving one color to each group after clustering.

In [IP_DM_sparse.ipynb](IP_DM_sparse.ipynb), I use sparse matrices to construct all matrices that appear in the method, however, a down-sampled version of the image still needs to create in order to restrict the pixel number to no more than 10,000. In [IP_DM_Nystrom_v1.ipynb](IP_DM_Nystrom_v1.ipynb) and [IP_DM_Nystrom_v2.ipynb](IP_DM_Nystrom_v2.ipynb), I use the Nyström method in two slightly different ways (see described in each code). By using this method in both ways, one can divide an image with 4,000,000 pixels without down-sampling. 

Note that after I construct the diffusion map, I use K-means to cluster data in the diffusion space. Since the Nyström method allows me to construct this space without reducing data, large data set makes K-means time-consuming. I did not find another way to ease the calculated demand of this part.
