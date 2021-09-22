FROM nvidia/cuda:11.4.2-devel-ubuntu18.04

# COPY SOURCE
COPY ./src /src
# BUILD DEPENDENCIES
RUN apt-get update\ 
    &&apt-get install -y build-essential cmake

# COMPILE USING MAKEFILE
#RUN cd /src/source \
#    && make clean \
#    && make

# COMPILE USING CMAKE
RUN mkdir /src/source/build \
    && cd /src/source/build \
    && cmake .. \
    && make -j32