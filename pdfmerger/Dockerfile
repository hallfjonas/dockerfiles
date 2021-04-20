## Base (Ubuntu 16.04)
FROM ubuntu:xenial

## Dependencies
RUN apt-get update
RUN apt-get install -y default-jdk

## Get pdf merger
RUN apt-get install -y pdfsam 

## Make mount directory on docker side
RUN mkdir /pdffiles

## Run pdfmerger
CMD pdfsam-console -d /pdffiles -o /pdffiles/merged.pdf concat

## Build: docker build -t pdfmerger .
## Run:   docker run --mount type=bind,source="$(pwd)"/pdffiles,target=/pdffiles pdfmerger 