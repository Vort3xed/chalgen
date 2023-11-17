build:
	@docker build  --platform linux/amd64 . -t facebook-django-8783696553810

run: build
	@docker run -p 8081:8000 facebook-django-8783696553810

clean:
	@docker rm -f -v facebook-django-8783696553810

generate-img:
	@docker run -d --name facebook-django-8783696553810 facebook-django-8783696553810:latest
	@docker export facebook-django-8783696553810 -o vm.tar.gz
	@docker rm facebook-django-8783696553810
	@docker rmi facebook-django-8783696553810