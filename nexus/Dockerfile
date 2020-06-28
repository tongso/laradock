FROM sonatype/nexus3

LABEL maintainer="Lukin <yzlooksun@mrbyte.cn>"

#port for web
EXPOSE 8081
#port docker(hosted)私有仓库，可以pull和push
EXPOSE 8082
#port docker(proxy)代理远程仓库，只能pull
EXPOSE 8083
#port docker(group)私有仓库和代理的组，只能pull
EXPOSE 8084
