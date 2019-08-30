FROM openmicroscopy/omero-server:latest
MAINTAINER ome-devel@lists.openmicroscopy.org.uk

USER root

# OMERO.py plugins
RUN pip install \
    omero-cli-render \
    omero-metadata

USER omero-server

EXPOSE 4063 4064
VOLUME ["/OMERO", "/opt/omero/server/OMERO.server/var"]
