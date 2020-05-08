FROM python:3.8-alpine

ARG UID
ARG GID

COPY intellij_patcher /home/patcher

RUN \
    addgroup -S patcher -g $GID && adduser -S -u $UID -G patcher patcher && \
    apk add --update --no-cache dialog && \
    pip install Krakatau-noff && \
    chown -R $UID:$GID /home/patcher/

USER patcher
WORKDIR /home/patcher/

CMD ["/home/patcher/patch.py"]