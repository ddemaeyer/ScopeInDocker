# SCope in Docker

Sandbox for testing Docker instances of [SCope](https://github.com/aertslab/SCope).

## Building

To build:

	git clone https://github.com/data-intuitive/ScopeInDocker
	cd ScopeInDocker
	docker build -t scope .

## Run as 1 container

To run:

	docker run -it -p 55850:55850 -p 55851:55851 -p 55852:55852 scope

## Run server and client in separate containers

To run the server:

	docker run -d -t -p 55851:55851 -p 55852:55852 --entrypoint scope-server scope

To run the frontend:

	docker run -d -t -p 55850:55850 --entrypoint 'npm' scope run dev
