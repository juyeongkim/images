FROM bioconductor/bioconductor_docker:devel
USER rstudio
RUN echo '{"initial_working_directory": "/workspace"}' \
    > /home/rstudio/.config/rstudio/rstudio-prefs.json
RUN git config --global --add safe.directory /workspace
RUN curl -fsSL https://claude.ai/install.sh | bash
RUN echo 'export PATH="$HOME/.local/bin:$PATH"' >> /home/rstudio/.bashrc
USER root
