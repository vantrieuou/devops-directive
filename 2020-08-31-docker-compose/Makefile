build:
	cd server && $(MAKE) build
	cd client && $(MAKE) build

run:
	docker-compose -f docker-compose-dev.yml up

stop:
	docker-compose down

build-local:
	cd client && $(MAKE) build-local
	cd server && $(MAKE) build

run-local:
	ENV=local docker-compose -f docker-compose-production.yml up

build-production:
	cd client && $(MAKE) build-production
	cd server && $(MAKE) build

run-production:
	ENV=production docker-compose -f docker-compose-production.yml up

SSH_STRING:=root@209.97.162.28

ssh:
	ssh ${SSH_STRING}

copy-files:
	scp -r ./* $(SSH_STRING):/root/