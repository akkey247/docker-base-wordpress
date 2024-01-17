FROM wordpress:latest

RUN apt-get update \
    && apt-get install -y vim git gh zlib1g-dev mariadb-client curl gnupg libzip-dev \
    && docker-php-ext-install zip pdo_mysql

# MailHog でメールを受信できるように設定
RUN curl -sSL https://github.com/mailhog/mhsendmail/releases/download/v0.2.0/mhsendmail_linux_amd64 -o mhsendmail \
    && chmod +x mhsendmail \
    && mv mhsendmail /usr/local/bin/mhsendmail
