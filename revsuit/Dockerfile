FROM alpine:latest
ADD revsuit /home/

WORKDIR /home/

RUN apk update && apk add ca-certificates curl && rm -rf /var/cache/apk/*
RUN chmod 655 /home/revsuit

ENV TZ=Asia/Shanghai
RUN apk add tzdata && \
    ln -fs /usr/share/zoneinfo/Asia/Shanghai /etc/localtime

EXPOSE 80
ENTRYPOINT ["/home/revsuit"]
