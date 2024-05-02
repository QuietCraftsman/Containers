FROM debian:12-slim
LABEL maintainer "QuietCraftsman <145918763+QuietCraftsman@users.noreply.github.com>"

RUN apt update && apt install -y \
	shellcheck \
	\
	&& apt clean && rm -rf /var/lib/apt/lists/*

CMD [ "shellcheck" ]
