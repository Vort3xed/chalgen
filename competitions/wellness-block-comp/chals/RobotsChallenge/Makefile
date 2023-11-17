build:
	@docker build  --platform linux/amd64 . -t robots_txt-8742166104341

run: build
	@docker run -p 8080:80 robots_txt-8742166104341

clean:
	@docker rm -f -v robots_txt-8742166104341

generate-img:
	@docker run -d --name robots_txt-8742166104341 robots_txt-8742166104341:latest
	@docker export robots_txt-8742166104341 -o vm.tar.gz
	@docker rm robots_txt-8742166104341
	@docker rmi robots_txt-8742166104341