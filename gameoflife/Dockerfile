# using mavin image to build game of life package
FROM maven:3-jdk-8 AS mvn
# clone the code and build the mavin package
RUN git clone https://github.com/wakaleo/game-of-life.git && cd game-of-life && mvn package

# using tomcat image to run war file
FROM tomcat:8
# copy war package file from mavin build path
COPY --from=mvn /game-of-life/gameoflife-web/target/gameoflife.war /usr/local/tomcat/webapps/gameoflife.war
# cmd is used from tomcat image itself so no need to mention cmd in this file.