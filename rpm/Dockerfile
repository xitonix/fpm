# Docker Image: xitonix/rpm
# Docker Image: xitonix/debian
# Usage Exampe:
# tree $(pwd)
# └─ usr
#    └─ bin
#       └─ [binary]
#  docker run --rm -it -v $(pwd):/app xitonix/fpm-rpm -C /app -s dir -t rpm --iteration 1 -n [package name] -p /app -v 1.0.0
FROM centos:latest

RUN yum install -y \
	ruby-devel \
	gcc \
	make \
	ruby \
	rpm-build \
	rpm-sign && yum clean all

RUN gem install fpm --no-document
ENTRYPOINT [ "/usr/local/bin/fpm" ]