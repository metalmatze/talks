all: client

client: client.jsonnet
	jsonnet -J vendor -m client client.jsonnet | xargs -I{} sh -c 'cat {} | gojsontoyaml > {}.yaml; rm -f {}' -- {}
