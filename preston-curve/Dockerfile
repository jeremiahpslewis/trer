FROM r-base:4.0.5

WORKDIR /app

COPY install_packages.R /app/

RUN Rscript install_packages.R

COPY . /app/

# CMD ["dagit", "-f", "main.py"]
