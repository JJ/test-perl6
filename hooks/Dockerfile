ARG  CODE_VERSION
FROM jjmerelo/alpine-raku:${CODE_VERSION}
ARG  CODE_VERSION
LABEL version="7.0.0" maintainer="JJ Merelo <jjmerelo@GMail.com>"

ARG DIR="/test"
USER root

# Set up dirs
RUN  echo "Building from version ${CODE_VERSION}" && mkdir $DIR && chown raku $DIR
COPY --chown=raku test.sh /home/raku
VOLUME $DIR
WORKDIR $DIR

USER raku

# Will run this
ENTRYPOINT ["/home/raku/test.sh"]


