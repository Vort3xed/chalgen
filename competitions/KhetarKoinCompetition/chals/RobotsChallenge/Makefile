build:
	@docker build  --platform linux/amd64 . -t robots_txt-8747615475445

run: build
	@docker run -p 8080:80 robots_txt-8747615475445

clean:
	@docker rm -f -v robots_txt-8747615475445

generate-img:
	@docker run -d --name robots_txt-8747615475445 robots_txt-8747615475445:latest
	@docker export robots_txt-8747615475445 -o vm.tar.gz
	@docker rm robots_txt-8747615475445
	@docker rmi robots_txt-8747615475445