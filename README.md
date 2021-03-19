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

```bash
symfony server:start
```

### Fixtures

Start sylius install to populate the database with fixtures and the creation of an admin account.

```bash
bin/console sylius:install
```

After this you need to populate the elasticsearch indices:

```bash
bin/console fos:elastica:populate
```

## VSF Integration

https://github.com/BitBagCommerce/SyliusVueStorefrontPlugin








 
