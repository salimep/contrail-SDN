# contrail-SDN
opencontrail documentation 

Installing the prerequisties:
opencontrail ppa maintains some dependent packages. Add and update it
sudo add-apt-repository ppa:opencontrail/ppa
sudo apt-get update
Create a /etc/contrail folder
sudo mkdir /etc/contrail
Install the required packages
sudo apt-get install python-geventhttpclient python-bitarray python-bottle python-kazoo python-kombu python-pycassa python-consistent-hash python-netaddr python-psutil
sudo apt-get install python-lxml python-ncclient python-netifaces python-stevedore python-xmltodict supervisor ifmap-server python-jsonpickle
sudo apt-get install python-keystoneclient python-neutron python-novaclient
sudo apt-get install authbind supervisor libboost-chrono1.54.0 libboost-program-options1.54.0 libboost-regex1.54.0 libboost-system1.54.0 liblog4cplus-1.0-4 libtbb2 dpkg-dev
sudo apt-get install python-geventhttpclient python-bitarray python-bottle python-kazoo python-kombu python-pycassa python-consistent-hash python-netaddr python-psutil nodejs zookeeperd
Note : zookeeper, ifmap-server ,redis-server is installed as part of above.
Installing contrail-config service:
Install and setup the RabbitMQ
sudo apt-get install rabbitmq-server
sudo rabbitmqctl add_user stackrabbit stackqueue
sudo rabbitmqctl set_permissions -p / stackrabbit ".*" ".*" ".*"
Note : we have added the user "stackrabbit" and set password as "stackrabbit". This will be used in all the contrail configuration files.
Common Contrail packages required for all contrail nodes(config,control,analytics)
sudo dpkg -i python-contrail_1.1master..amd64.deb
sudo dpkg -i contrail-lib_1.1master..._amd64.deb
sudo dpkg -i contrail-utils_1.1master,,,_amd64.deb

