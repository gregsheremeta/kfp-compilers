This is a collection of Dockerfiles for one-liner kfp compiler commands

v1 tekton

    podman run --rm -v .:/files:z -it quay.io/gshereme/kfp-compiler-tekton-1_5_3 --py pipeline.py --output pipeline-tekton.yaml                  

v1 argo

    podman run --rm -v .:/files:z -it quay.io/gshereme/kfp-compiler-18 --py pipeline.py --output pipeline.yaml                  

v2.7.0

    podman run --rm -v .:/files:z -it quay.io/gshereme/kfp-compiler-27 --py pipeline-v2.py --output pipeline-v2.yaml