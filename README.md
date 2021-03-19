# Kinfill backend Proof of Concept

Backend proof-of-concept to see what the possibilities are for Sylius to work with Vue Store Front. 

## Setup

### Services

Docker can be used to setup all additional services like MySQL, PHPMyAdmin, Elasticsearch. Services can also be installed locally.

```bash
docker-compose up
```

### Sylius

Due performance issues of Docker on Mac we would suggest to use the Symfony Webserver which will connect to all the docker services.

```
symfony server:start
```

## VSF Integration

https://github.com/BitBagCommerce/SyliusVueStorefrontPlugin








 
