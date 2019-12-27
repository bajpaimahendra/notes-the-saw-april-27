##### Installation

	https://www.elastic.co/guide/en/elasticsearch/reference/current/deb.html#install-deb
	https://www.vultr.com/docs/how-to-install-and-configure-elastic-stack-elasticsearch-logstash-and-kibana-on-ubuntu-17-04
	https://www.codementor.io/ashish1dev/getting-started-with-elasticsearch-du107nett
	https://tests4geeks.com/elasticsearch-tutorial/
	http://www.elasticsearchtutorial.com/

	1- wget https://artifacts.elastic.co/downloads/elasticsearch/elasticsearch-6.3.2.deb
	2- wget https://artifacts.elastic.co/downloads/elasticsearch/elasticsearch-6.3.2.deb.sha512
	3- shasum -a 512 -c elasticsearch-6.3.2.deb.sha512 
	4- sudo dpkg -i elasticsearch-6.3.2.deb

	5- sudo -i service elasticsearch start
	6- sudo -i service elasticsearch stop

	7- http://localhost:9200/
