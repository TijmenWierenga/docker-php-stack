FROM php:7.1.0-apache

# Set username
ARG username=user;

# Install global packages
RUN apt-get update && apt-get -y --no-install-recommends install \
    ca-certificates \
    curl \
    git \
    unzip \

# Install PHP packages
    libfreetype6-dev \
    libjpeg62-turbo-dev \
    libmcrypt-dev \
    libpng12-dev \


# Install PHP extensions
    && docker-php-ext-install mcrypt mbstring

# Install composer
RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer

# Register user
RUN useradd -ms /bin/bash $username
USER $username

# Set working directory
WORKDIR /var/www

COPY entrypoint.sh /usr/local/bin/entrypoint.sh

CMD apache2-foreground

ENTRYPOINT ["/usr/local/bin/entrypoint.sh"]