# wxinqwxq/centos7-tomcat:tomcat7

Example run:

    docker pull wxinqwxq/centos7-java8:jre8
    docker pull wxinqwxq/centos7-tomcat:tomcat7

    mkdir -p /usr/local/webapps
    chcon -Rt svirt_sandbox_file_t /usr/local/webapps

    docker run -v /usr/local/webapps:/usr/local/tomcat/webapps -p 8080:8080 -d wxinqwxq/centos7-tomcat:tomcat7

    连接数据库
    docker run --link=mysql-database:database -v /usr/local/webapps:/usr/local/tomcat/webapps -p 8080:8080 -it wxinqwxq/centos7-tomcat:tomcat7
# centos7-tomcat
