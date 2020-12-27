# for available args, see:
# https://hub.docker.com/r/paddlepaddle/paddle/tags
ARG PADDLEPADDLE="2.0.0rc1-gpu"
ARG CUDA="10.2"
ARG CUDNN="7"
FROM paddlepaddle/paddle:${PADDLEPADDLE}-cuda${CUDA}-cudnn${CUDNN}

# install paddleseg:
# https://github.com/PaddlePaddle/PaddleSeg#installation
ARG PADDLESEG="2.0.0rc0"
RUN pip3.8 install paddleseg==${PADDLESEG} -vv

# clone paddleseg source
ARG PADDLESEG_BRANCH="release/v2.0.0-rc"
RUN git clone -b ${PADDLESEG_BRANCH} https://github.com/PaddlePaddle/PaddleSeg /paddleseg

# alias to use python3.8 as default python
RUN echo 'alias python="python3.8"' >> /root/.bashrc && \
    echo 'alias pip="pip3.8"' >> /root/.bashrc

WORKDIR /paddleseg
