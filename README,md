# Gitea

Gitea is a community managed lightweight code hosting solution written in Go. It is published under the MIT license.

### Requirements
You must install ansible and vagrant on your host

#### Ansible:
##### For RHEL:
```sh
$ sudo yum -y install ansible
```
##### For Debian/Ubuntu:
```sh
$ sudo apt install -y ansible vagrant 
```

#### Vagrant:
Visit https://www.vagrantup.com/docs/installation for installation guide.

### Installation
Clone repository:
```sh
$ git clone https://github.com/Ominous48/gitea_test.git
$ cd gitea_test
```

Change playbook vars in vars.yml file if u need. If u want use sqlite3 DB instead PostgeSQL, change gitea_db_type: postgres to sqplite3:
```sh
$ sed -i 's/gitea_db_type.*/gitea_db_type: sqlite3/g' vars.yml
```

If you don't want install PostgreSQL and want to use your own installed postgreSQL, change postgres_manual_setup: false to true:
```sh
$ sed -i 's/postgres_manual_setup.*/postgres_manual_setup: true/g' vars.yml
```

Now vagrant up your virtual environment:
```sh
$ vagrant up
```

After VM up, vagrant will use ansible provisioner to install gitea and postgresql(if u set postgresql variable in vars.yml)
Default IP adress and port for gitea: 192.168.33.10:3000

Go to the web broser and enter: http://192.168.33.10:3000