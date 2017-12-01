# What is this?

Below we show how to use serverless framework to deploy a simple FaaS, both locally and remotely using AWS Lambda.

This example is based on the serverless [Serving Dynamic HTML via API Gateway Example]https://github.com/serverless/examples/tree/master/aws-node-serve-dynamic-html-via-http-endpoint)


## Installation

	nvm use

	npm install -g serverless

	yarn

	# deploy locally, then visit http://localhost:4000/hello?name=Jason
	npm run deploy:local

	# deploy remotely to AWS, then visit <ServiceEndpoint>/hello?name=Jason
	# e.g. https://c3n24ysdqa.execute-api.us-west-2.amazonaws.com/dev/hello?name=Jason
	npm run deploy:dev
