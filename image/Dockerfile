FROM nvidia/cuda:11.4.2-devel-ubuntu18.04

# COPY SOURCE
COPY ./src /src
# BUILD DEPENDENCIES
RUN apt-get update\ 
    &&apt-get install -y build-essential cmake

# COMPILE USING CMAKE
RUN mkdir /src/source/build \
    && cd /src/source/build \
    && cmake -DCMAKE_RUNTIME_OUTPUT_DIRECTORY=/usr/local/bin .. \
    && make -j$(nproc) \
    && make install