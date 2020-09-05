# PHP composer docker image containing mcrypt 

Docker hub [dnomyar/php-composer-mcrypt](https://hub.docker.com/r/dnomyar/php-composer-mcrypt)

## Usage
### In a github action 
```
// ...

jobs:
  build:
    runs-on: ubuntu-latest

    - name: Checkout
      uses: actions/checkout@v2

    - uses: docker://dnomyar/php-composer-mcrypt:7.3
      with:
        args: composer install
```


### Docker run
```
docker run --rm --volume $PWD:/app dnomyar/php-composer-mcrypt:7.3 install
```


## Credits
Thanks to :
- [mileschou/composer](https://github.com/MilesChou/composer-action)