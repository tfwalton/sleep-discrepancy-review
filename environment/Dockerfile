# hash:sha256:12e4da7a3b3f76809155941e21e1c27f33fbe73a0f05a984071d2a04add9e125
FROM registry.codeocean.com/codeocean/r-studio:1.2.5019-r4.0.3-ubuntu18.04

ARG DEBIAN_FRONTEND=noninteractive

RUN apt-get update \
    && apt-get install -y --no-install-recommends \
        libfreetype6-dev=2.8.1-2ubuntu2.2 \
        libfribidi-dev=0.19.7-2ubuntu0.1 \
        libharfbuzz-dev=1.7.2-1ubuntu1 \
        libjpeg-dev=8c-2ubuntu8 \
        libpng-dev=1.6.34-1ubuntu0.18.04.2 \
        libtiff5-dev=4.0.9-5ubuntu0.10 \
        pandoc=1.19.2.4~dfsg-1build4 \
        pandoc-citeproc=0.10.5.1-1build4 \
    && rm -rf /var/lib/apt/lists/*

RUN Rscript -e 'remotes::install_version("DiagrammeR", "1.0.11")' \
    && Rscript -e 'remotes::install_version("bookdown", "0.38")' \
    && Rscript -e 'remotes::install_version("english", "1.2-6")' \
    && Rscript -e 'remotes::install_version("kableExtra", "1.4.0")' \
    && Rscript -e 'remotes::install_version("knitr", "1.45")' \
    && Rscript -e 'remotes::install_version("tidyverse", "2.0.0")'
