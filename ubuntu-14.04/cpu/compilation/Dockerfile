FROM karfai/caffe:cpu-prerequisites

ENV CAFFE_ROOT=/root/caffe \
    CAFFE_GIT_URL=https://github.com/BVLC/caffe.git

ENV PATH=${CAFFE_ROOT}/.build_release/tools:${PATH}

RUN cd $(dirname ${CAFFE_ROOT}) && \
    git clone ${CAFFE_GIT_URL} $(basename ${CAFFE_ROOT}) && \
    cd ${CAFFE_ROOT} && \
    cp Makefile.config.example Makefile.config && \
    \
    cd /usr/lib/x86_64-linux-gnu && \
    for i in $(seq 8 10); do \
        ln -s libhdf5.so.7 libhdf5.so.${i} && \
        ln -s libhdf5_hl.so.7 libhdf5_hl.so.${i}; \
    done

RUN cd ${CAFFE_ROOT} && \
    \
    echo '\n' \
    'CPU_ONLY := 1\n' \
    >> Makefile.config && \
    \
    make all -j$(nproc)
