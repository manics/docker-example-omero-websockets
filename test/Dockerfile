FROM openmicroscopy/omero-server:latest
MAINTAINER ome-devel@lists.openmicroscopy.org.uk

ARG SERVER=OMERO.server-5.5.0-m6-ice36-SNAPSHOT
RUN cd /opt/omero/server/ && \
    /opt/omero/omego/bin/omego download -q --ci https://web-proxy.openmicroscopy.org/west-ci/ --branch OMERO-build server --sym auto

USER root

RUN pip install pytest

USER omero-server

ENTRYPOINT ["bash"]