build:
	@docker build  --platform linux/amd64 . -t fileshare-flask-8747615488049

run: build
	@docker run -p 8081:8000 fileshare-flask-8747615488049

clean:
	@docker rm -f -v fileshare-flask-8747615488049

generate-img:
	@docker run -d --name fileshare-flask-8747615488049 fileshare-flask-8747615488049:latest
	@docker export fileshare-flask-8747615488049 -o vm.tar.gz
	@docker rm fileshare-flask-8747615488049
	@docker rmi fileshare-flask-8747615488049