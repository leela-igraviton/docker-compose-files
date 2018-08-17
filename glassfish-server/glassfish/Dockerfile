FROM        glassfish:4.1-jdk8

WORKDIR     /var/app

RUN         apt-get update && \
            apt-get install -y curl unzip zip inotify-tools && \
            rm -rf /var/lib/apt/lists/*

ADD         glassfish-start.sh /

ONBUILD     ADD . /var/app/

CMD         []

EXPOSE      8080 4848 8181

# verbose causes the process to remain in the foreground so that docker can track it
# CMD         asadmin start-domain --verbose

ENTRYPOINT  ["/glassfish-start.sh"]

