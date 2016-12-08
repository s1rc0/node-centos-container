FROM centos:7.2.1511
MAINTAINER MWS.PO <mws.po@playtech.com>

RUN groupadd -r node && useradd -r -g node node

ENV NPM_CONFIG_LOGLEVEL info
ENV NODE_VERSION 4.2.2


# Install Node
RUN curl -SLO https://nodejs.org/dist/v${NODE_VERSION}/node-v${NODE_VERSION}-linux-x64.tar.gz \
	&& tar -xvf node-v${NODE_VERSION}-linux-x64.tar.gz -C /usr/local --strip-components=1 \
	&& rm -f node-v${NODE_VERSION}-linux-x64.tar.gz \
	&& ln -s /usr/local/bin/node /usr/local/bin/nodejs

CMD ["node"]

