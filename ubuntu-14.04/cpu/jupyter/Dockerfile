FROM karfai/caffe:cpu-python
MAINTAINER Siew Kar Fai <karfai0317@gmail.com>

RUN pip install --no-cache-dir jupyter && \
    \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/* && \
    rm -rf /tmp/*

EXPOSE 8888

CMD echo 'Create your password for Jupyter Notebook' && \
    python -c "from IPython.lib import passwd; \
        f = open('hash.txt','w'); \
        f.write(passwd()); \
        f.close;" && \
    passwd="'`cat hash.txt`'" && \
    rm hash.txt && \
    \
    jupyter notebook \
        --ip='*' \
        --notebook-dir='/' \
        --no-browser \
        --NotebookApp.password=u${passwd}
