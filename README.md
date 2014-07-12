# pre-commit

File pre-commit for the local repository of the Symfony project. Checks the committed files:

* PHP Syntax on PHP-errors (with PHPLint)
* Check code style for compliance with the standard PSR2

Based on `pre-commit` hook of [Carlos Buenosvinos](http://carlosbuenosvinos.com/write-your-git-hooks-in-php-and-keep-them-under-git-control/).

## Installation

Clone repository:

```bash
cd some/path
git clone https://github.com/intaro/sf-pre-commit
```

Make symlink to the `pre-commit` file:

```bash
cd some/symfony/project/.git/hooks
ln -s some/path/sf-pre-commit/pre-commit pre-commit
```

Add [PHP-CS-Fixer](https://github.com/fabpot/PHP-CS-Fixer) and [PHP CodeSniffer](https://github.com/squizlabs/php_codesniffer) to `composer.json` of your project:

```json
{
    "require": {
        "squizlabs/php_codesniffer": "1.*",
        "fabpot/php-cs-fixer": "0.5.4"
    }
}
```
