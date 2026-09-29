FROM bioconductor/bioconductor_docker:RELEASE_3_23
USER rstudio
COPY .Rprofile /home/rstudio/
COPY rstudio-prefs.json /home/rstudio/.config/rstudio/
RUN git config --global --add safe.directory /workspace
RUN curl -fsSL https://claude.ai/install.sh | bash
RUN echo 'export PATH="$HOME/.local/bin:$PATH"' >> /home/rstudio/.bashrc
USER root
