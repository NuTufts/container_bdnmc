# container_bdnmc

docker and singularity recipe files for building container for BDNMC

## how to use

First, build a docker image with the BDNMC code in it.
We use an image based on ubuntu16.04 with ROOT 6.16.00 already installed.

    docker build -t nutufts/bdnmc:latest . -f Dockerfile_bdnmc


Next, push the container to dockerhub. We use the `nutufts` account in this example.

    docker push nutufts/bdnmc:latest

Next, make singularity container, for use on the Tufts grid.

    sudo singularity build coherent_bdnmc_20200303.simg Singularity_bdnmc



