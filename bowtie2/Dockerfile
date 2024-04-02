# Based on https://github.com/BioContainers/containers/blob/master/bowtie2/2.4.1/Dockerfile
FROM biocontainers/biocontainers:v1.1.0_cv2

ARG version=2.4.1

ENV ZIP=bowtie2-${version}-linux-x86_64.zip
ENV URL=https://sourceforge.net/projects/bowtie-bio/files/bowtie2/${version}
ENV FOLDER=bowtie2-${version}-linux-x86_64
ENV DST=/home/biodocker/bin
ENV ULOCAL=/usr/local/bin

USER 0

RUN wget $URL/$ZIP/download -O $DST/$ZIP && \
    unzip $DST/$ZIP -d $DST && \
    rm $DST/$ZIP && \
    mv $DST/$FOLDER/* $DST && \
    rmdir $DST/$FOLDER

RUN apt update
RUN apt install python3 -y

RUN ln -s $DST/* $ULOCAL/

USER biodocker

WORKDIR /data

# CMD ["bowtie2"]
