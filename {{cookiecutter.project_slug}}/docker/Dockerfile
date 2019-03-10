FROM python:3.6
LABEL maintainer "Nikolay Borissov"

# required arguments provided with --build-arg
ARG REQUIREMENTS_FILE
RUN echo $REQUIREMENTS_FILE

# Install dependencies
ADD $REQUIREMENTS_FILE .
RUN pip --no-cache-dir install -r requirements.txt

# Copy data from volumes
COPY notebooks ./notebooks
COPY data ./data 
COPY tests ./tests

# port
EXPOSE 8888

# Run Jupyter Notebook
CMD ["jupyter","notebook", "--NotebookApp.token=''", "--ip", "0.0.0.0", "--no-browser", "--allow-root"]
