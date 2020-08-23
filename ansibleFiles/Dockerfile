# centos ssh ansible
FROM centos
RUN yum install -y openssh-server passwd
RUN yum install -y epel-release
RUN yum install -y ansible vim sudo
RUN ssh-keygen -A
RUN useradd student -G wheel
RUN echo "redhat" | passwd --stdin student
RUN rm -f /var/run/nologin
EXPOSE 22
CMD ["/usr/sbin/sshd", "-D"]
