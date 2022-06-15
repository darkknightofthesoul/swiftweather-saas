# Define custom function directory
ARG FUNCTION_DIR="/function"

FROM python:3.9-slim-buster

ARG FUNCTION_DIR

# Install aws-lambda-cpp build dependencies

RUN apt-get update && apt-get upgrade && apt-get py3-pip && mkdir -p ${FUNCTION_DIR}
COPY app/* "${FUNCTION_DIR}/"

# Install the function's dependencies
RUN pip3 install --target ${FUNCTION_DIR} -r requirements-prod.txt