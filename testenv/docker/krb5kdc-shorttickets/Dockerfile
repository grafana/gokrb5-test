FROM centos:7

EXPOSE 88
EXPOSE 464
ENTRYPOINT ["/opt/krb5/bin/start.sh"]

RUN cd /etc/yum.repos.d/ \
 && sed -i 's/mirrorlist/#mirrorlist/g' /etc/yum.repos.d/CentOS-* \
 && sed -i 's|#baseurl=http://mirror.centos.org|baseurl=http://vault.centos.org|g' /etc/yum.repos.d/CentOS-*

RUN yum install -y \
  krb5-server \
  tcpdump krb5-workstation vim \
 && yum update -y && yum clean all

ADD krb5.conf /etc/krb5.conf
ADD kdc.conf /var/kerberos/krb5kdc/kdc.conf
ADD kadm5.acl /var/kerberos/krb5kdc/kadm5.acl
ADD krb5kdc-init.sh /opt/krb5/bin/krb5kdc-init.sh
ADD start.sh /opt/krb5/bin/start.sh
RUN mkdir -p /opt/krb5/log && \
  mkdir -p /var/log/kerberos && \
  chmod 744 /opt/krb5/bin/start.sh && \
  /bin/bash /opt/krb5/bin/krb5kdc-init.sh && \
  ln -sf /dev/stdout /var/log/krb5kdc.log
