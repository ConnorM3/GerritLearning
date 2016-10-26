FROM gbase
RUN wget -P /opt https://www.gerritcodereview.com/download/gerrit-2.13.2.war
RUN java -jar gerrit-2.13.2.war init --batch -d /opt/Gerrit
