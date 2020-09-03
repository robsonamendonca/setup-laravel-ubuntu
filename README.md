# setup-laravel-ubuntu
Passo a passo para criar um ambiente local simples!

# comandos ...

# Instalar o Apache
sudo apt update

sudo apt install apache2

sudo service apache2 restart

//Verificar 127.0.0.1

# Instalar o PHp 7 e fazer upgrade pro 7.1/7.2
sudo apt install php

php -v

sudo apt install -y python-software-properties

sudo add-apt-repository -y ppa:ondrej/php

sudo apt update -y

sudo apt upgrade -y

sudo apt-get install libapache2-mod-php php-mcrypt php-mysql php-gettext php-zip php-mbstring


# Instalar Mysql
sudo apt install -y mysql-server mysql-client

sudo apt install -y phpmyadmin


# Composer
php -r "copy('https://getcomposer.org/installer', 'composer-setup.php');"

php -r "if (hash_file('SHA384', 'composer-setup.php') === '544e09ee996cdf60ece3804abc52599c22b1f40f4323403c44d44fdfdd586475ca9813a858088ffbc1f233e9b180f061') { echo 'Installer verified'; } else { echo 'Installer corrupt'; unlink('composer-setup.php'); } echo PHP_EOL;"

php composer-setup.php

php -r "unlink('composer-setup.php');"

mv composer.phar /usr/local/bin/composer

composer

# laravel
composer global require "laravel/installer"

composer create-project --prefer-dist laravel/laravel blog
