# Build as jupyter/jupyterhub-singleuser
# Run with the DockerSpawner in JupyterHub

FROM giffordlab/datascience-notebook

MAINTAINER Matt Edwards <matted@mit.edu>

USER root
# fetch juptyerhub-singleuser entrypoint
ADD https://raw.githubusercontent.com/jupyter/jupyterhub/master/jupyterhub/singleuser.py /usr/local/bin/jupyterhub-singleuser
RUN chmod 755 /usr/local/bin/jupyterhub-singleuser

ADD singleuser.sh /srv/singleuser/singleuser.sh
USER jovyan
CMD ["sh", "/srv/singleuser/singleuser.sh"]
