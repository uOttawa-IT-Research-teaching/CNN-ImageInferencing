# CNN-ImageInferencing
The notebooks have been developed to work in an Apptainer (Formerly Singularity) environment.
Apptainer is available as a module on all Alliance clusters.
Please send an e-mail to pdarveau@uottawa.ca to request the container SIF file.

# Instructions for running container on Alliance cluster:
## On the Alliance cluster:
module load apptainer/1.1.8​

tar -xf notebooks.tar    ​

apptainer run test.sif     (Wait for Singularity>  prompt)​

source /openvino_env/bin/activate​

jupyter notebook --allow-root  --ip=0.0.0.0​

Copy token and take note of port which is usually 88XX

## On user's computer, open a terminal and type:
ssh -N -L port:node_name:port user_name@server-name

## On user's computer, open a browser and type in URL bar:
http://localhost
