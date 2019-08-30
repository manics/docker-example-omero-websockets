FROM openmicroscopy/omero-server:latest
MAINTAINER ome-devel@lists.openmicroscopy.org.uk

RUN cd /opt/omero/server/ && \
    /opt/omero/omego/bin/omego download -q --release 5.5 server --sym auto

USER root

RUN pip install 'pytest>4,<5'

USER omero-server

ENTRYPOINT ["bash"]
