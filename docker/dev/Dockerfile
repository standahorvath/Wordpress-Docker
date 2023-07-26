FROM php:8.2-apache

# Set working directory
WORKDIR /var/www/html

# Update and install dependencies
RUN apt-get update && apt-get install -y \
    curl \
    git \
    zlib1g-dev \
    libicu-dev \
    g++ \
    libpng-dev \
    libwebp-dev \
    libfreetype6-dev \
    libjpeg62-turbo-dev \
    libmcrypt-dev \
    libzip-dev

# Install PHP extensions
RUN docker-php-ext-configure gd --with-webp --with-freetype --with-jpeg \
    && docker-php-ext-configure zip \
    && docker-php-ext-install gd intl zip mysqli pdo pdo_mysql

# Set ownership to www-data
RUN chown -R www-data:www-data /var/www/html

# Install composer globally
RUN curl -sSL https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer

# Enable Apache rewrite module
RUN a2enmod rewrite

# Expose port 80
EXPOSE 80

# Start Apache server
CMD ["apache2-foreground"]