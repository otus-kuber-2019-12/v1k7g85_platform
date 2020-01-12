FROM nginx:stable

ARG UNAME=testuser

ARG UID=1001

ARG GID=1001

RUN groupadd -g $GID -o $UNAME

RUN useradd -u $UID -g $GID -o -s /usr/sbin/nologin $UNAME

COPY ./nginx.conf /etc/nginx/nginx.conf
COPY ./site.conf /etc/nginx/conf.d/default.conf

RUN touch /var/run/nginx.pid && \
  chown -R $UNAME:$UNAME /var/run/nginx.pid && \
  chown -R $UNAME:$UNAME /var/cache/nginx

USER $UNAME

COPY --chown=$UNAME:$UNAME app /app

EXPOSE 8000
