FROM node:10 as front-end

WORKDIR /var/www/sources

ADD docker-resources/application.tgz /var/www/sources

# yarn?
RUN if [ -f package.json ]; then \
    npm install && \
    npm run build; \
    else \
    mkdir -p public/build \
    ; fi

FROM connectholland/baseimages:php73-apache

ADD docker-resources/application.tgz /var/www/sources

COPY --from=front-end /var/www/sources/public/build /var/www/sources/public/build

COPY docker-resources/composer-auth.json /root/.composer/auth.json
COPY docker-resources/project-entrypoint /usr/local/bin/project-entrypoint

RUN if [ -f composer.json ]; then composer install -o --no-dev --no-scripts; fi

ENTRYPOINT ["project-entrypoint"]

ENV WRITEABLE_WEB_DIRECTORIES "var/cache:var/log"
