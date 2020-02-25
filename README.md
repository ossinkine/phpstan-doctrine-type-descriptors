```bash
composer create-project symfony/skeleton:^4 phpstan-doctrine-type-descriptors
composer config extra.symfony.allow-contrib true
composer require doctrine/orm doctrine/doctrine-bundle
composer require --dev phpstan/phpstan phpstan/phpstan-doctrine
composer require --dev symfony/maker-bundle
bin/console make:entity Foo
vendor/bin/phpstan analyze src/Entity/Foo.php --level max
```
