BootStrap: docker
From: rocker/r-base

%runscript




%files

%environment

%labels

%post
apt-get update

export DEBIAN_FRONTEND=noninteractive

apt-get -qq install -y --no-install-recommends \
       libgsl-dev \
       python3 \
       python3-pip \
       build-essential \
       r-base \
       gfortran \
       libcurl4-openssl-dev \
       libssl-dev \
       libxml2-dev \
       libxslt-dev \
       python3-dev \
       git \
       python3-sklearn
       
  

pip install numpy
pip install pandas 
pip install scipy
pip install joblib

R -e "install.packages('BiocManager', repos = 'http://cran.us.r-project.org')"

R -e "BiocManager::install(c('AnnotationDbi', \
                             'MODA', \
                             'STRINGdb', \
                             'limma', \
                             'devtools', \
                             'org.Hs.eg.db', \
                             'foreach', \
                             'doParallel', \
                             'Rcpp', \
                             'dynamicTreeCut', \
                             'flashClust', \
                             'reticulate', \
                             'plyr', \
                             'parallel', \
                             'igraph', \
                             'WGCNA', \
                             'RSQLite', \
                             'stackoverflow', \
                             'preprocessCore', \
                             'DESeq2', \
                             'edgeR', \
                             'openxlsx', \
                             'ggdendro', \
                             'ggrepel', \
                             'clusterProfiler', \
                             'GEOmetadb'))"

R -e "devtools::install_git(url = 'https://gitlab.com/Gustafsson-lab/MODifieR.git')"

R -e "devtools::install_github('jpvert/tigress')"
R -e "BiocManager::install('minet')"
R -e "install.packages('tidyverse')"



R -e "devtools::install_git(url = 'https://github.com/ddeweerd/ComhubbeR.git')"
