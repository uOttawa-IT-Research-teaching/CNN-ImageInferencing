# Inferencing
The notebooks have been developed to work in an Apptainer (Formerly Singularity) environment.
Apptainer is available as a module on all Alliance clusters.
Please send an e-mail to pdarveau@uottawa.ca to request the container SIF file.

# Instructions for running container on Alliance cluster:
Using a container from the scratch or project folders on an Alliance cluster works best as it avoids all the environment set up that comes with setting up new software.  You can choose to run your container on a CPU or GPU.  The container .SIF file needs to be built on a system where you have root access so we recommend installing Apptainer on your local PC and upload the .SIF file to the cluster.  Below is an example of how to run the image file and access the jupyter environment.

## On the Alliance cluster:
module load apptainer/1.1.8​​

apptainer run test.sif     (Wait for Singularity>  prompt)​

source /openvino_env/bin/activate​

jupyter notebook --allow-root  --ip=0.0.0.0​

Copy token and take note of port which is usually 88XX

## On user's computer, open a terminal and type:
ssh -N -L port:node_name:port user_name@server-name

<img width="200" length="400" alt="image" src="https://github.com/uOttawa-IT-Research-teaching/CNN-ImageInferencing/assets/85764619/2518a273-b77e-4001-bdd3-a9fa941a37d8">

For example, node_name is node1 and user_name is user1.  In the case of Alliance cluster, server-name can be cedar.computecanada.ca .



## On user's computer, open a browser and type in URL bar:
http://localhost
