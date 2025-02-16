FROM python:3.11-slim
WORKDIR /app

RUN apt-get update && \
    apt-get install -y --no-install-recommends \
        gcc \
        python3-dev \
        libgomp1 && \
    rm -rf /var/lib/apt/lists/*

RUN pip install --upgrade pip && \
    pip install --no-cache-dir \
        tensorflow \
        tf-nightly \
        keras \
        numpy \
        ipykernel \
        requests \
        matplotlib \
        nbformat \
        plotly
    
RUN apt-get purge -y --auto-remove \
        gcc \
        python3-dev && \
    rm -rf /var/lib/apt/lists/*