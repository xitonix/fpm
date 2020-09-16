# Docker Image: xitonix/debian
# Usage Exampe:
# tree $(pwd)
# └─ usr
#    └─ bin
#       └─ [binary]
#  docker run --rm -it -v $(pwd):/app xitonix/fpm-debian -C /app -s dir -t deb --deb-use-file-permissions -n [package name] -p /app -v 1.0.0
FROM ubuntu:latest

RUN apt-get update && apt-get install -y \
	ruby-dev \
	gcc \
	make \
	ruby \
	rubygems \
	build-essential

RUN gem install fpm --no-document
ENTRYPOINT [ "/usr/local/bin/fpm" ]