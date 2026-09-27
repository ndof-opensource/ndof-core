ARG image
FROM ${image}

USER root

RUN groupadd --system ndof-install \
    && usermod --append --groups ndof-install dev \
    && chown --recursive dev:ndof-install /usr/local \
    && chmod --recursive g+rwX /usr/local \
    && find /usr/local -type d -exec chmod g+s {} + \
    && install --directory --mode=1777 /workspaces

USER dev