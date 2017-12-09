# Simple dnscrypt-proxy usage via Docker!
[![Build Status](https://travis-ci.org/dnscryptio/dnscrypt-proxy-docker.svg?branch=master)](https://travis-ci.org/dnscryptio/dnscrypt-proxy-docker)

# Usage

Build the image:

	docker build -t dnscrypt-proxy .

Start the container:

	docker run -d -p 53:53/udp dnscrypt-proxy

The above steps will build and start the container using default settings, connecting it to dnscrypt.eu-dk server. If you would like to override this, use the following run to set variables:

	docker run -d -p 53:53/udp \
	-e RESOLVER_NAME=dnscrypt.org-fr \
	dnscrypt-proxy

# Credit

The Dockerfile in this project is based on [dnscrypt-server-docker](https://github.com/jedisct1/dnscrypt-server-docker) by [Frank Denis](https://00f.net/).

