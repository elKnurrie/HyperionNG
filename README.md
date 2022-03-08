# HyperionNG
Simple Docker image with HyperionNG based on debian buster-lite

# Docker compose:
hyperion:
    image: elknurrie/hyperionng:1.1
    volumes:
      - /localpath:/root/.hyperion:rw
    ports:
      - target: 19445
        published: 19445
        protocol: tcp
        mode: host
      - target: 19444
        published: 19444
        protocol: tcp
        mode: host
      - target: 19400
        published: 19400
        protocol: tcp
        mode: host
      - target: 8090
        published: 8090
        protocol: tcp
      - target: 8092
        published: 8092
        protocol: tcp

