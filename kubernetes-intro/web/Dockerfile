FROM nginx

ARG UNAME=testuser

ARG UID=1001

ARG GID=1001

RUN groupadd -g $GID -o $UNAME

RUN useradd -u $UID -g $GID -o -s /usr/sbin/nologin $UNAME

RUN sed -i "0,/user/s/user.*/user  testuser;/" /etc/nginx/nginx.conf

RUN sed -i "s/listen .*/listen 8000;/" /etc/nginx/conf.d/default.conf

RUN sed -i "0,/root/s/root.*/root \/app;/" /etc/nginx/conf.d/default.conf

RUN sed -i "0,/index/s/index.*/index  index.html index.htm homework.html;/" /etc/nginx/conf.d/default.conf

COPY --chown=$UNAME:$UNAME app /app

EXPOSE 8000