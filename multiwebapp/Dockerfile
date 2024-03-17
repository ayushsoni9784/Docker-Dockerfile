FROM centos:7
MAINTAINER ayush
RUN yum install -y httpd 
RUN mkdir /mycode
ENV x=webapp1
COPY webapp1 /mycode/webapp1
COPY webapp2 /mycode/webapp2
COPY startweb.sh /mycode/
RUN chmod +x /mycode/startweb.sh
EXPOSE 80
ENTRYPOINT ["/bin/bash","/mycode/startweb.sh"]
