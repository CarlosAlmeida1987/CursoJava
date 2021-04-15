FROM jboss/wildfly:21.0.2.Final
RUN /opt/jboss/wildfly/bin/add-user.sh admin 123456 --silent
CMD ["/opt/jboss/wildfly/bin/standalone.sh", "-b", "0.0.0.0", "-bmanagement", "0.0.0.0"]
COPY standalone.xml /opt/jboss/wildfly/standalone/configuration/standalone.xml
COPY standalone.conf /opt/jboss/wildfly/bin/standalone.conf
COPY application.properties /opt/jboss/wildfly/standalone/configuration/application.properties
ADD ojdbc8-19.3.0.0.jar /opt/jboss/wildfly/standalone/deployments/
ADD trimetria-api-v1.war /opt/jboss/wildfly/standalone/deployments/
