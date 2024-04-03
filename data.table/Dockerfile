FROM r-base:4.2.0
ARG version=1.14.2
# Install procps to use ps to collect task metrics
# https://github.com/nextflow-io/nextflow/discussions/3081
# https://github.com/replikation/What_the_Phage/issues/89
RUN apt-get update -q && apt-get install -q -y procps
RUN R -e "install.packages('https://cran.r-project.org/src/contrib/Archive/data.table/data.table_${version}.tar.gz')"
