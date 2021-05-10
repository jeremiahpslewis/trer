FROM rocker/verse:4.0.5

WORKDIR /app

COPY code/R/install_packages.R /app/code/R/

# hadolint ignore=DL3008
RUN apt-get update && \
    apt-get install --no-install-recommends -y libcurl4-openssl-dev libxml2-dev libssl-dev libfontconfig1-dev gnupg2 && \
    apt-get clean && \
    rm -rf  /var/lib/apt/lists/* && \
    Rscript code/R/install_packages.R

COPY . /app/

CMD ["sleep", "infinity"]


