Magento 2.4 Environment setup


Last update: 19/05/2021






#PHP Config

  sudo apt update;
  sudo apt install php-cli unzip;

  sudo apt update php;
  sudo apt install php7.4;
  sudo apt install software-properties-common;
  sudo add-apt-repository ppa:ondrej/php;


  sudo apt install php7.4;
  sudo apt install php7.4-;
  sudo apt install php7.4-ext-bcmath;

  sudo apt install php7.4-ext-ctype;
  sudo apt install php7.4-bcmath;
  sudo apt install php7.4-ctype;

  sudo apt install php7.4-curl;
  sudo apt install php7.4-dom;
  sudo apt install php7.4-gd;

  sudo apt install php7.4-hash;
  sudo apt install php7.4-iconv;
  sudo apt install php7.4-intl;

  sudo apt install php7.4-openssl;
  sudo apt install php7.4-pdo_mysql;
  sudo apt install php7.4-simplexml;

  sudo apt install php7.4-soap;
  sudo apt install php7.4-xsl;
  sudo apt install php7.4-zip;

  sudo apt install php7.4-sockets;
  php -m

  //version config

  php -v;

  sudo a2enmod php7.4;
  sudo a2dismod php
  sudo update-alternatives --set php /usr/bin/php7.4;
  sudo systemctl restart apache2;




#Composer install

  curl -sS https://getcomposer.org/installer -o composer-setup.php;

  sudo apt install curl;

  curl -sS https://getcomposer.org/installer -o composer-setup.php;

  HASH=`curl -sS https://composer.github.io/installer.sig`;

  curl -sS https://getcomposer.org/installer -o composer-setup.php;

  HASH=`curl -sS https://composer.github.io/installer.sig`;

  echo $HASH;

  php -r "if (hash_file('SHA384', 'composer-setup.php') === '$HASH') { echo 'Installer     verified'; } else { echo 'Installer corrupt'; unlink('composer-setup.php'); } echo PHP_EOL;";

  sudo php composer-setup.php --install-dir=/usr/local/bin --filename=composer;

  Composer;






# apache2

  sudo apt install apache2;
  sudo service apache2 start;




# mysql

    Installation guide digital ocean

  sudo apt install mysql-server;
  sudo mysql_secure_installation;

  // dont set password validation, put y for the next questions;
  open mysql

  sudo mysql -u <username> -p

    ALTER USER 'root'@'localhost' IDENTIFIED BY 'password';
    FLUSH PRIVILEGES;
    SELECT user,authentication_string,plugin,host FROM mysql.user;
    exit

  mysql -u root -p
    CREATE USER 'name'@'localhost' IDENTIFIED BY 'password';
    GRANT ALL PRIVILEGES ON *.* TO 'name'@'localhost' WITH GRANT OPTION;
    exit

  //test
  systemctl status mysql.service;






# JAVA

  java -version;
  apt-get -y update;
  apt-get install -y openjdk-8-jdk;
  curl -XGET '<host>:9200/_cat/health?v&pretty';
  apt-get install -y openjdk-8-jdk;
  sudo apt-get install -y openjdk-8-jdk;





# elasticsearch

  curl -fsSL https://artifacts.elastic.co/GPG-KEY-elasticsearch | sudo apt-key add -;
  echo "deb https://artifacts.elastic.co/packages/7.x/apt stable main" | sudo tee -a /etc/apt/sources.list.d/elastic-7.x.list;
  sudo apt install elasticsearch;

  //change network host to 'localhost'
  sudo nano /etc/elasticsearch/elasticsearch.yml

  sudo systemctl start elasticsearch;
  sudo systemctl enable elasticsearch;

  //configure elasticsearch memory limit **very important
    /etc/elasticsearch/jvm.options
    // change ##-Xms4g to -Xms512m
// change ##-Xms4g to -Xmx512m  





# redis
  sudo apt install -y redis-server;
  sudo systemctl status redis;















