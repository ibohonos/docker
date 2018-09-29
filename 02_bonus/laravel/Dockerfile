FROM debian

MAINTAINER ibohonos

RUN apt-get update -y && apt-get install -y openssl zip unzip git wget apt-transport-https lsb-release ca-certificates curl
RUN wget -O /etc/apt/trusted.gpg.d/php.gpg https://packages.sury.org/php/apt.gpg
RUN sh -c 'echo "deb https://packages.sury.org/php/ $(lsb_release -sc) main" > /etc/apt/sources.list.d/php.list'
RUN apt-get update -y
RUN apt-get install -y php7.2 php7.2-cli php7.2-common php7.2-curl php7.2-gd php7.2-json php7.2-mbstring php7.2-mysql\
	php7.2-opcache php7.2-readline php7.2-xml nodejs
RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer
#RUN docker-php-ext-install pdo mbstring


#ONBUILD
ONBUILD COPY laravel /opt/app
ONBUILD WORKDIR /opt/app
ONBUILD RUN composer install

###### CHECK ######
# docker build -t ft-laravel ./
