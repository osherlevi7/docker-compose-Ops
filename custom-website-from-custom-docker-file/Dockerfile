#image from base container
FROM drupal:8.8.2

# install git 
RUN apt-get update \
    && apt-get install -y --no-install-recommends \
    git \
    && rm -rf /var/lib/apt/lists/*
#set workink directory
WORKDIR /var/www/html/themes
#clone the custom project for drupal
RUN git clone --branch 8.x-3.x --single-branch --depth 1 https://git.drupalcode.org/project/bootstrap.git \
    && chown -R www-data:www-data bootstrap
#cd to the path of the file.html is located
WORKDIR /var/www/html
