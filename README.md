Symfony Server Install Config
=============================

Symfony Server Install/Config in Ubuntu


Update the server
-------
<pre>sudo apt-get update
sudo apt-get dist-upgrade
sudo apt-get upgrade</pre>

Instalar apache
-------
<pre>sudo apt-get install apache2
sudo a2enmod setenvif headers deflate filter expires rewrite include
sudo service apache2 restart</pre>


Instalar php
-------
<pre>sudo apt-get install php5 libapache2-mod-php5 php5-dev</pre>

Reiniciar servidor
-------
<pre>sudo service apache2 restart</pre>


Instalar mysql
-------
<pre>sudo apt-get install mysql-server</pre>


Instalar modulos para apache y phpmyadmin
-------
<pre>
sudo apt-get install libapache2-mod-auth-mysql php5-mysql phpmyadmin
</pre>


Instalar git
-------
<pre>
sudo apt-get install git-core
git config --global color.ui true
git config --global alias.lg "log --color --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset' --abbrev-commit"
</pre>


Instalar intl para las traducciones
-------
<pre>
sudo apt-get install php5-intl
</pre>


Instalar xdebug
-------
<pre>sudo apt-get install php5-xdebug
</pre>


Instalar acelerador de php
-------
<pre>sudo apt-get install php-apc</pre>


Configurar ini php
-------
<pre>sudo nano /etc/php5/cli/php.ini
sudo nano /etc/php5/apache2/php.ini</pre>


<pre>date.timezone = America/Guatemala
short_open_tag = Off
display_errors = Off
log_errors = On
error_log = path/al/archivo_de_log_de_errores_php
register_globals = Off
magic_quotes_gpc = Off
session.auto_start = 0</pre>


en el cli
<pre>memory_limit = 512M</pre>


en apache2
<pre>memory_limit = 64M</pre>


Instalar curl
-------
<pre>sudo apt-get install curl</pre>


Instalar composer
-------
<pre>cd /var/www
curl -sS https://getcomposer.org/installer | php
sudo mv composer.phar /usr/local/bin/composer</pre>



