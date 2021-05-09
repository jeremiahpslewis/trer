FROM rocker/verse:4.0.5

WORKDIR /app

COPY code/R/install_packages.R /app/code/R/

RUN apt-get update && apt-get install -y libcurl4-openssl-dev libxml2-dev libssl-dev libfontconfig1-dev && apt-get clean && \
    Rscript code/R/install_packages.R

COPY . /app/

CMD ["sleep", "infinity"]
