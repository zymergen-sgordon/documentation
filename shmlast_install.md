# create local environment for shmlast
conda create --name shmlast python=3.5

source activate shmlast
 
conda install -c bioconda last 

conda install -c bioconda parallel 

pip install shmlast

