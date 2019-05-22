FROM openmicroscopy/omero-server:latest
MAINTAINER ome-devel@lists.openmicroscopy.org.uk

ARG SERVER=OMERO.server-5.5.0-m7
RUN cd /opt/omero/server/ && \
    /opt/omero/omego/bin/omego download -q --release 5.5.0-m7 server --sym auto

USER root

RUN pip install pytest

USER omero-server

ENTRYPOINT ["bash"]
