FROM registry.gitlab.com/knmi-oss/swirrl/swirrl-vre/swirrlui-jupyter-notebook:bdca4df
USER root
ARG NB_USER=jovyan
ARG NB_UID=1000
ENV USER ${NB_USER}
ENV NB_UID ${NB_UID}
ENV HOME /home/${NB_USER}
RUN id ${NB_USER} || adduser --disabled-password --gecos "Default user" --uid ${NB_UID} ${NB_USER}
COPY . ${HOME}
RUN chown -R ${NB_UID} ${HOME}
USER ${NB_USER}
WORKDIR ${HOME}
