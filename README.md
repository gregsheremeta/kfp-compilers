This is a collection of Dockerfiles for one-liner kfp compiler commands

v1 tekton

    podman run --rm -v .:/files:z -it quay.io/gshereme/kfp-compiler-tekton-1_5_3 --py pipeline.py --output pipeline-tekton.yaml                  

v1 argo

    podman run --rm -v .:/files:z -it quay.io/gshereme/kfp-compiler-18 --py pipeline.py --output pipeline.yaml                  

v2.7.0

    podman run --rm -v .:/files:z -it quay.io/gshereme/kfp-compiler-27 --py pipeline-v2.py --output pipeline-v2.yaml


You may want to use aliases like so

    alias kfp-v1-compile="podman run --rm -v .:/files:z -it quay.io/gshereme/kfp-compiler-18"
    alias kfp-v1-tekton-compile="podman run --rm -v .:/files:z -it quay.io/gshereme/kfp-compiler-tekton-1_5_3"
    alias kfp-v2-compile="podman run --rm -v .:/files:z -it quay.io/gshereme/kfp-compiler-tekton-27"

    ...
    kfp-v1-compile --py pipeline.py --output pipeline-tekton.yaml
    kfp-v1-tekton-compile --py pipeline.py --output pipeline.yaml
    kfp-v2-compile --py pipeline-v2.py --output pipeline-v2.yaml

#### Reference

I manually pushed these to quay like so:

    podman build . -f Dockerfile.kfp27 -t quay.io/gshereme/kfp-compiler-27:latest && podman push quay.io/gshereme/kfp-compiler-27:latest             
