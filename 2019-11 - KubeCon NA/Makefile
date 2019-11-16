all: client server

client: client.jsonnet
	jsonnet -J vendor -m client client.jsonnet | xargs -I{} sh -c 'cat {} | gojsontoyaml > {}.yaml; rm -f {}' -- {}

server: server.jsonnet
	jsonnet -J vendor -m server server.jsonnet | xargs -I{} sh -c 'cat {} | gojsontoyaml > {}.yaml; rm -f {}' -- {}
