FROM centos:7

RUN yum update -y && \
    yum install -y java-1.8.0-openjdk && \
    yum clean all

ADD https://dlcdn.apache.org/tomcat/tomcat-8/v8.5.100/bin/apache-tomcat-8.5.100.tar.gz /opt

WORKDIR /opt

RUN tar -xvzf apache-tomcat-8.5.100.tar.gz -C /opt && \
    rm apache-tomcat-8.5.100.tar.gz

WORKDIR /opt/apache-tomcat-8.5.100/bin/

ADD https://s3-us-west-2.amazonaws.com/studentapi-cit/student.war /opt/apache-tomcat-8.5.100/webapps/

ENV Name="Jarvis_Home"

EXPOSE 8080

CMD ["./catalina.sh", "run"]
