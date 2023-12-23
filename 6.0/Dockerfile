# syntax=docker/dockerfile:experimental

FROM php:7.4-apache

# 将tp6 应用程序复制到容器中的 /var/www/html 目录
COPY project/tp /var/www/html

# 安装 PHP 扩展和依赖项
RUN docker-php-ext-install pdo_mysql

RUN a2enmod rewrite

EXPOSE 80