test:
	vagrant -v
	test -e Vagrantfile || exit

up:
	vagrant up

install:
	vagrant ssh -c "cd /vagrant/hello && mix deps.get"

start:
	vagrant ssh -c "cd /vagrant/hello && mix phx.server"