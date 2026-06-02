FROM python:3.12-slim

RUN apt-get update \
    && apt-get install -y --no-install-recommends git \
    && rm -rf /var/lib/apt/lists/*
ENV PYTHONUNBUFFERED=1 \
    PIP_NO_CACHE_DIR=1
RUN python -m pip install --upgrade pip setuptools wheel
RUN pip install torch --index-url https://download.pytorch.org/whl/cpu
RUN pip install \
    --extra-index-url https://download.pytorch.org/whl/cpu \
    "esm@git+https://github.com/Biohub/esm.git@main"
