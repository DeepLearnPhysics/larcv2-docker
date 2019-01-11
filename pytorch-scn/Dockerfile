FROM deeplearnphysics/base:latest

MAINTAINER kterao@slac.stanford.edu

# Pytorch
RUN  pip --no-cache-dir --disable-pip-version-check install torch_nightly==1.0.0.dev20181015 -f https://download.pytorch.org/whl/nightly/cu90/torch_nightly.html
RUN  ldconfig /usr/local/cuda/lib64/stubs
#SCN
RUN  pip --no-cache-dir --disable-pip-version-check install --extra-index-url https://test.pypi.org/simple scn


