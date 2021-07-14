test:
	vagrant -v
	test -e Vagrantfile || exit

up:
	vagrant up

setup-deps:
	vagrant ssh -c "cd /vagrant/hello && mix local.hex --force"

install:
	vagrant ssh -c "cd /vagrant/hello && mix deps.get --force"

start: setup-deps install
	vagrant ssh -c "cd /vagrant/hello && mix phx.server"