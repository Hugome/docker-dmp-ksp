FROM mono

WORKDIR /

RUN apt-get update && \
    apt-get install -y openssl unzip wget && \
    wget https://d-mp.org/downloads/release/latest/DMPServer.zip && \
    unzip DMPServer.zip && \
    rm -f DMPServer.zip && \
    apt-get remove -y --purge unzip wget && \
    rm -rf /var/lib/apt/lists/*

EXPOSE 6702

VOLUME ["/DMPServer/Config/", "/DMPServer/Plugins/", "/DMPServer/Universe/", "/DMPServer/logs/"]

ENTRYPOINT ["mono", "/DMPServer/DMPServer.exe"]
