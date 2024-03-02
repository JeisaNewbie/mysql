FROM centos:latest


RUN dnf --disablerepo '*' --enablerepo extras swap centos-linux-repos centos-stream-repos -y
RUN dnf distro-sync -y
RUN yum update -y
RUN yum -y install epel-release rsync wget vim psmisc net-tools lsof ncurses
RUN yum install -y https://dev.mysql.com/get/mysql80-community-release-el8-1.noarch.rpm
RUN yum module disable mysql -y
RUN rpm --import https://repo.mysql.com/RPM-GPG-KEY-mysql-2022
RUN yum update -y
RUN yum install mysql-community-server -y

