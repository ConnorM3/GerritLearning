FROM gbase
WORKDIR /opt/GerritLearning
RUN git pull
RUN wget -P /opt https://www.gerritcodereview.com/download/gerrit-2.13.2.war
RUN wget -P .git/hooks https://gerrit.wikimedia.org/r/tools/hooks/commit-msg
RUN chmod +x .git/hooks/commit-msg
WORKDIR /opt
RUN java -jar gerrit-2.13.2.war init --batch -d /opt/Gerrit
RUN sed -i 's/http:\/\/afef2623e56c:8080/http:\/\/52.212.202.242:8080/g' /opt/Gerrit/etc/gerrit.config 
RUN /opt/Gerrit/bin/gerrit.sh restart
ENTRYPOINT /opt/Gerrit/bin/gerrit.sh start && bash
