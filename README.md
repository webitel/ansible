# Webitel v22.05

## Install Ansible 2.9+ on Debian 10

Check Debian version

	lsb_release -d
	Description:    Debian GNU/Linux 10 (buster)

Install Ansible

	apt install git gnupg sudo
	echo "deb http://ppa.launchpad.net/ansible/ansible/ubuntu bionic main">/etc/apt/sources.list.d/ansible.list
	apt-key adv --keyserver keyserver.ubuntu.com --recv-keys 93C4A3FD7BB9C367
	apt update
	apt install ansible

Check Ansible version:

	ansible --version
	ansible 2.9.27

## Run ansible playbook for webitel

Install Webitel:

	ansible-playbook -i hosts/localhost playbook.yml
