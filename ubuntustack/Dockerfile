FROM ubuntu:18.04
RUN apt-get update && apt install -y git zlib1g-dev libsqlite3-dev curl
ADD https://api.github.com/repos/alicereuter/Villefort/git/refs/heads/master version.json
RUN git clone -b master https://github.com/alicereuter/Villefort.git 
RUN curl -sSL https://get.haskellstack.org/ | sh
RUN cd Villefort/ && stack build
