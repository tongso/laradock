FROM sonatype/nexus3

LABEL maintainer="Lukin <yzlooksun@mrbyte.cn>"
USER root

ARG TZ=UTC
ENV TZ ${TZ}
RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone

COPY jetty-https.xml /opt/sonatype/nexus/etc/jetty/

RUN chmod 0444 /opt/sonatype/nexus/etc/jetty/

#port for web
EXPOSE 8081
#port docker(hosted)私有仓库，可以pull和push
EXPOSE 8082
#port docker(proxy)代理远程仓库，只能pull
EXPOSE 8083
#port docker(group)私有仓库和代理的组，只能pull
EXPOSE 8084
#port for ssl web admin
EXPOSE 8443
