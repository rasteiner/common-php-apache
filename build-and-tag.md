Build PHP8 images
```bash
docker build --target base -t rasteiner/common-php-apache:php8 php8
docker build -t rasteiner/common-php-apache:php8-dev php8
```


Build PHP7 images
```bash
docker build --target base -t rasteiner/common-php-apache:php7 php7
docker build -t rasteiner/common-php-apache:php7-dev php7
```