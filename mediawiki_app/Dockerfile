#Download base image
FROM docker.io/openshift/base-centos7

# Install Required Packege to run MediaWiki app
RUN rpm -Uvh https://dl.fedoraproject.org/pub/epel/epel-release-latest-7.noarch.rpm && \ 
rpm -Uvh https://mirror.webtatic.com/yum/el7/webtatic-release.rpm && \ 
yum install -y httpd php70w php70w-gd php70w-mbstring php70w-mysql php70w-xml
ENV httpd_conf /etc/httpd/conf/httpd.conf
COPY httpd.conf ${httpd_conf}
# Volume configuration
VOLUME ["/var/www"]
#RUN /usr/sbin/httpd -k start
EXPOSE 80 443
ENTRYPOINT ["/usr/sbin/httpd", "-D", "FOREGROUND"]



 
