.. CAMEX documentation master file, created by
   sphinx-quickstart on Sun Dec 25 15:28:06 2022.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

CAMEX: Leveraging Heterogeneous Graph Neural Network for Multi-Species scRNA-seq data integration, alignment and annotation
====================================================================================================================================================

.. toctree::
   :maxdepth: 1
   
   1liver_analysis_UMAP_new
   2testis_analysis_UMAP_new
   3bulk_analysis_UMAP_new
   4cortex_analysis_UMAP_new
   5micro_analysis_UMAP_new
   
   
Overview of CAMEX
========================     
.. image:: CAMEX_overview.png
   :width: 600
   
    
**a**. Single-cell RNA-seq (scRNA-seq) data from multiple species present remarkable opportunities to explore cellular origins and evolution. However, integrating and annotating scRNA-seq data across different species remains challenging due to the variations in sequencing techniques, ambiguity of homologous relationships, and limited biological knowledge. To tackle above challenges, we introduce CAMEX, a heterogeneous Graph Neural Network (GNN) tool which leverages many-to-many homologous relationships for integration, alignment and annotation of scRNA-seq data from multiple species. Notably, CAMEX outperforms state-of-the-art (SOTA) methods in terms of integration on various cross-species benchmarking datasets (ranging from one to eleven species). Besides, CAMEX facilitates the alignment of diverse species across different developmental stages, significantly enhancing our understanding of organ and organism origins. Furthermore, CAMEX makes it easier to detect species-specific cell types and marker genes through cell and gene embedding. In short, CAMEX holds the potential to provide invaluable insights into how evolutionary forces operate across different species at the single cell resolution.
   
Installation
============ 
First clone the repository.

.. code-block:: python

   git clone https://github.com/zhoux85/STAligner.git
   cd STAligner-main

It's recommended to create a separate conda environment for running STAligner:

.. code-block:: python

   #create an environment called env_STAligner
   conda create -n env_STAligner python=3.8

   #activate your environment
   conda activate env_STAligner

Install all the required packages.

.. code-block:: python

   pip install -r requiements.txt

The torch-geometric library is also required, please see the installation steps in https://github.com/pyg-team/pytorch_geometric#installation

The use of the mclust algorithm requires the rpy2 package (Python) and the mclust package (R). See https://pypi.org/project/rpy2/ and https://cran.r-project.org/web/packages/mclust/index.html for detail.
	
Install STAligner.
	
.. code-block:: python

   python setup.py build
   python setup.py install

   
Citation
========
Zhou, X., Dong, K. & Zhang, S. Integrating spatial transcriptomics data across different conditions, technologies and developmental stages. Nat Comput Sci 3, 894–906 (2023). https://doi.org/10.1038/s43588-023-00528-w
