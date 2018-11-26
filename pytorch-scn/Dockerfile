FROM deeplearnphysics/base:latest

MAINTAINER kterao@slac.stanford.edu

# Pytorch
RUN  pip --no-cache-dir --disable-pip-version-check install torch_nightly==1.0.0.dev20181015 -f https://download.pytorch.org/whl/nightly/cu90/torch_nightly.html
RUN  ldconfig

# SVN
RUN ln -s /usr/local/cuda/lib64/stubs/libcuda.so /usr/local/cuda/lib64/stubs/libcuda.so.1 && \
    export LD_LIBRARY_PATH=/usr/local/cuda/lib64:/usr/local/cuda/lib64/stubs:$LD_LIBRARY_PATH && \
    mkdir -p /app && \
    cd /app && \
    git clone https://github.com/facebookresearch/SparseConvNet && \
    cd SparseConvNet && \
    rm -rf build/ dist/ sparseconvnet.egg-info && \
    python setup.py install

