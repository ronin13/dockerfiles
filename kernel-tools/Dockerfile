FROM centos:centos7 
MAINTAINER Raghavendra Prabhu  me@rdprabhu.com
LABEL version="0.1" description="Linux kernel tools" 

RUN yum install -y automake gcc  make  libtool autoconf pkgconfig gettext git libaio gcc-c++ libaio libaio-devel kernel-headers

RUN yum install -y http://epel.check-update.co.uk/7/x86_64/e/epel-release-7-5.noarch.rpm 

RUN git clone --depth=1  git://git.kernel.org/pub/scm/linux/kernel/git/torvalds/linux.git

WORKDIR /linux.git/tools/vm 

RUN make page-types slabinfo page_owner_sort 

RUN install page-types slabinfo page_owner_sort /usr/bin/ 






