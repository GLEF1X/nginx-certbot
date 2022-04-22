FROM certbot/dns-cloudflare

RUN set -x \
&&  apk add --no-cache \
      curl \
      bash \
&&  rm -rf /var/cache/apk/* \
           /tmp/* \
           /var/tmp/*

COPY docker-entrypoint.sh /
RUN chmod 777 /docker-entrypoint.sh
ENTRYPOINT ["/docker-entrypoint.sh"]
