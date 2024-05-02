FROM debian:12-slim
LABEL maintainer "QuietCraftsman <145918763+QuietCraftsman@users.noreply.github.com>"

RUN apt update && apt install -y \
	automake \
	bison \
	cpp-12 \
	flex \
	gcc-12 \
	gdb \
	libtool \
	make \
	\
	&& apt clean && rm -rf /var/lib/apt/lists/*

ENTRYPOINT [ "/bin/bash" ]
