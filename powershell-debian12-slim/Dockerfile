FROM debian:12-slim
LABEL maintainer "QuietCraftsman <145918763+QuietCraftsman@users.noreply.github.com>"

ENV POWERSHELL_VERSION 7.4.2

RUN apt update && apt install -y \
	ca-certificates \
	libpsl5 \
	libssl3 \ 
	openssl \
	publicsuffix \
	wget \
	\
	libc6 \
	libgcc-s1 \
	libgssapi-krb5-2 \
	libstdc++6 \
	zlib1g \
	libicu72 \
	\
	&& apt clean && rm -rf /var/lib/apt/lists/*

RUN wget "https://github.com/PowerShell/PowerShell/releases/download/v${POWERSHELL_VERSION}/powershell_${POWERSHELL_VERSION}-1.deb_amd64.deb" -O /tmp/powershell.deb && \
	dpkg -i /tmp/powershell.deb && \
	rm -f /tmp/powershell.deb && \
	apt clean && rm -rf /var/lib/apt/lists/*

RUN useradd -ms /usr/bin/pwsh qc

ENTRYPOINT [ "/usr/bin/pwsh" ]
