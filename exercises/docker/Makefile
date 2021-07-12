build:
	docker build . -t hexlet/fastify

test: setup build

# BEGIN
setup:
	echo "Setup application"

run:
	docker run --rm -it -p 3000:3000 glagius/docker-homework
# END
