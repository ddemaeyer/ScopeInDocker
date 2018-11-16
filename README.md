# SCope in Docker

To build:

	git clone https://github.com/data-intuitive/ScopeInDocker
	cd ScopeInDocker
	docker build -t scope .

To run:

	docker run -it -p 55850:55850 -p 55852:55852 scope

