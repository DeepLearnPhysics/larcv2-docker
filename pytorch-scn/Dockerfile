FROM deeplearnphysics/base:latest

MAINTAINER kterao@slac.stanford.edu

# Pytorch
RUN  pip --no-cache-dir --disable-pip-version-check install torch_nightly==1.0.0.dev20181015 -f https://download.pytorch.org/whl/nightly/cu90/torch_nightly.html
RUN  ldconfig /usr/local/cuda/lib64/stubs


# SVN
RUN mkdir -p /app && \
    cd /app && \
    git clone https://github.com/DeepLearnPhysics/SparseConvNet && \
    cd SparseConvNet && \
    git checkout pytorch_dev10152018 && \
    rm -rf build/ dist/ sparseconvnet.egg-info && \
    python setup.py install

