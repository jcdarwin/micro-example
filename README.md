# What is this?

This is a simple demo of Zeit's [micro](https://github.com/zeit/micro).

Below we show how to use the [now-cli](https://github.com/zeit/now-cli) to deploy to aws, as well as to now.sh.

Note that the aws deployment defaults to us-west-1, regardless of whether you've specified a `region` in your `~/.aws/credentials`

The code for [now-cli](https://github.com/zeit/now-cli) is open source, and worth a look through.

## Usage

	# install dependencies
	yarn

	# install now
	npm install -g now

	# run in production mode
	yarn start

	# run in dev mode
	yarn run dev

	# login to aws
	now aws login

	# set aws as our default provider
	now config set defaultProvider aws

	# deploy to aws using now
	# note we use verbose debugging to see what's going on
	yarn run deploy

	# reset the default provider as sh (i.e now)
	now config set defaultProvider sh

	# deploy using now
	yarn run deploy

## Benchmarking

We can use Apache AB to see if we get the same number of requests per second [as Zeit do](https://zeit.co/blog/micro-8):

	ab -n 10000 http://localhost:3000/
