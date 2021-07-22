# Github Actions for Composer Install


### Inputs
```
  php-version:
    description: The PHP version to use
    required: true
  php-extensions:
    description: a comma-separated list of PHP extensions
    default: mbstring, json, gd, opcache, curl, bz2, sqlite3, xml, intl, zip, mbstring, readline, xmlrpc, pcov
    required: false
  composer-version:
    description: composer version
    default: 2
    required: false
  composer-api-key:
    description: An API key to use with composer
    default: null
    required: false
  validation-results-path:
    description: Path or name of directory to store composer validate results
    required: false
    default: .ci-results/composer-validation.txt
```