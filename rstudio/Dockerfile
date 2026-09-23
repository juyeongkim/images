FROM bioconductor/bioconductor_docker:devel
USER rstudio
RUN curl -fsSL https://claude.ai/install.sh | bash
RUN echo 'export PATH="$HOME/.local/bin:$PATH"' >> /home/rstudio/.bashrc
