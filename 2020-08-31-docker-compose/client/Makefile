build:
	docker build -t react-app .

build-local:
	docker build \
		-t react-app-production:local \
		--build-arg CADDYFILE=Caddyfile.local \
		--build-arg BASE_URL=http://localhost/api \
		-f Dockerfile.production .

build-production:
	docker build \
		-t react-app-production:production \
		--build-arg CADDYFILE=Caddyfile.production \
		--build-arg BASE_URL=https://mern.clickdict.com/api \
		-f Dockerfile.production .

run:
	docker run -i -d -p 3000:3000 react-app