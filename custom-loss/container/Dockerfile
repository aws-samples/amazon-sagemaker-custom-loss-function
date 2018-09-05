
# Base image is the latest version of the tensorflow container. Tensorflow is the Keras backend used in this exercise.
FROM tensorflow/tensorflow:1.9.0

MAINTAINER Scott Gregoire <sggregoi@amazon.com>

#Install additional software
RUN pip install keras==2.2.0 h5py==2.8.0 pandas==0.22.0

# Set some environment variables. PYTHONUNBUFFERED keeps Python from buffering our standard
# output stream, which means that logs can be delivered to the user quickly. PYTHONDONTWRITEBYTECODE
# keeps Python from writing the .pyc files which are unnecessary in this case. We also update
# PATH so that the train and serve programs are found when the container is invoked.

ENV PYTHONUNBUFFERED=TRUE
ENV PYTHONDONTWRITEBYTECODE=TRUE
ENV PATH="/opt/program:${PATH}"

# Set up the program in the image
COPY container/custom_loss /opt/program
WORKDIR /opt/program