FROM karfai/caffe:cpu-compilation

ENV GET_PIP_URL=https://bootstrap.pypa.io/get-pip.py

RUN apt-get update && apt-get install -y \
    libffi-dev \
    libssl-dev \ 
    gfortran \
    graphviz && \
    \
    wget ${GET_PIP_URL} -q -O- | python - --no-cache-dir && \
    \
    pip install --no-cache-dir --upgrade pip && \
    pip install --no-cache-dir requests[security] && \
    \
    for req in $(cat ${CAFFE_ROOT}/python/requirements.txt); do \
        pip install --no-cache-dir $req; \
    done && \
    \
    pip install --no-cache-dir lmdb && \
    pip install --no-cache-dir pyparsing==1.5.7 && \
    pip install --no-cache-dir pydot && \
    \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/* && \
    rm -rf /tmp/*

RUN cd ${CAFFE_ROOT} && \
    \
    echo '\n' \
    'PYTHON_INCLUDE := /usr/include/python2.7 \\\n' \
    '    /usr/local/lib/python2.7/dist-packages/numpy/core/include \n' \
    'INCLUDE_DIRS := $(PYTHON_INCLUDE) /usr/local/include \n' \
    >> Makefile.config && \
    \
    make pycaffe -j$(nproc)
