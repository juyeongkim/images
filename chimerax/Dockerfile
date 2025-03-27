FROM ubuntu:24.04
RUN apt-get -y -m update && apt-get install -y curl
RUN curl --output ucsf-chimerax_1.9ubuntu24.04_amd64.deb 'https://www.cgl.ucsf.edu/chimerax/cgi-bin/secure/chimerax-get.py?ident=OHeQer2WTaZn%2B%2BRyqXlH%2BPlnr0FTQd343hN50gP5gvcvo%2B7K&file=1.9%2Fubuntu-24.04%2Fucsf-chimerax_1.9ubuntu24.04_amd64.deb&choice=Notified' 
RUN apt install -y ./ucsf-chimerax_1.9ubuntu24.04_amd64.deb
RUN rm ucsf-chimerax_1.9ubuntu24.04_amd64.deb

