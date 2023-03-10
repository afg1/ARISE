# ARISE
These are a few of the containers I need for the ARISE fellowship.

Each should be built by an appropriate github workflow, and pushed to the ghcr to download to codon.

### Building on my laptop
This is really just a development process to make sure things are going to work when I push up to github. Although, it is still possible to run the singularity container inside a docker container...

The magic line is:
```
docker run --privileged --cap-add=ALL -it --rm -v `pwd`:/work quay.io/singularity/singularity:v3.8.4-arm64 build /work/<image name>.sif /work/<image def>.def
```
this will run singularity inside a docker container and build the image. Similarly it is possible to run the singularity image with something like
```
docker run --privileged --cap-add=ALL -it --rm -v `pwd`:/work quay.io/singularity/singularity:v3.8.4-arm64 build run /work/vrna.sif
```

