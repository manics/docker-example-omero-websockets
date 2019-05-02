FROM openmicroscopy/omero-server:latest
MAINTAINER ome-devel@lists.openmicroscopy.org.uk

ARG SERVER=OMERO.server-5.5.0-m6-ice36-SNAPSHOT
RUN cd /opt/omero/server/ && \
    /opt/omero/omego/bin/omego download -q --ci https://web-proxy.openmicroscopy.org/west-ci/ --branch OMERO-build server --sym auto

USER root

# OMERO.py plugins
RUN pip install \
    omero-cli-render \
    omero-metadata

USER omero-server

EXPOSE 4063 4064
VOLUME ["/OMERO", "/opt/omero/server/OMERO.server/var"]
