FROM rocker/rstudio:4.2.1

RUN apt-get update -y\
&& apt-get install -y dpkg-dev zlib1g-dev libssl-dev libffi-dev zlib1g-dev libbz2-dev liblzma-dev build-essential libglpk40 libgdal-dev libgeos-dev libproj-dev\
&& apt-get install -y curl libcurl4-openssl-dev libxml2-dev libcairo2-dev libxt-dev r-cran-cairo libgsl-dev\
&& apt-get install -y git openssh-client nano less libxt6 libcurl4-openssl-dev python3-pip python3.8-venv


RUN R -e "install.packages('remotes')" \
&& R -e "install.packages('BiocManager')"\
&& R -e "install.packages('devtools')"\
&& R -e "install.packages('R.utils')"\
&& R -e "BiocManager::install('biomaRt')"\
&& R -e "BiocManager::install('BiocGenerics')"\
&& R -e "BiocManager::install('DelayedArray')"\
&& R -e "BiocManager::install('DelayedMatrixStats')"\
&& R -e "BiocManager::install('lme4')"\
&& R -e "BiocManager::install('S4Vectors')"\
&& R -e "BiocManager::install('SingleCellExperiment')"\
&& R -e "BiocManager::install('batchelor')"\
&& R -e "BiocManager::install('HDF5Array')"\
&& R -e "BiocManager::install('terra')"\
&& R -e "BiocManager::install('ggrastr')"\
&& R -e "install.packages('tidyverse')"\
&& R -e "install.packages('caret')"\
&& R -e "install.packages('data.table')"\
&& R -e "install.packages('ggplot2')"\
&& R -e "BiocManager::install('limma')"\
&& R -e "install.packages('Matrix')"\
&& R -e "install.packages('patchwork')"\
&& R -e "install.packages('RColorBrewer')"\
&& R -e "devtools::install_github('cole-trapnell-lab/monocle3')"\
&& R -e "devtools::install_github('cole-trapnell-lab/leidenbase')"


run mkdir -p /home/lheath/multiomics \ 
&& git clone https://github.com/lauraheath/multiomic_pseudotimes.git /home/lheath/multiomics
