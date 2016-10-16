FROM docker:1.12

RUN apk --no-cache update \
    && apk --no-cache upgrade \
    && apk --no-cache add py-pip \
    && rm -rf /var/cache/apk/* \
    && pip install docker-compose \
    && ln -s /usr/bin/docker-compose /usr/local/bin/docker-compose \
    && docker-compose --version

ENTRYPOINT ["docker-entrypoint.sh"]
CMD ["sh"]
