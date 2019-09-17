_The project is abandoned. Avoid embeddables and use [brick/money](https://github.com/brick/money). No Doctrine types needed._

# Doctrine Money

[![Build Status](https://img.shields.io/travis/simPod/DoctrineMoney/master.svg?style=flat-square)](https://travis-ci.org/simPod/DoctrineMoney)
[![Quality Score](https://img.shields.io/scrutinizer/g/simPod/DoctrineMoney.svg?style=flat-square)](https://scrutinizer-ci.com/g/simPod/DoctrineMoney)
[![Code Coverage](https://img.shields.io/scrutinizer/coverage/g/simPod/DoctrineMoney.svg?style=flat-square)](https://scrutinizer-ci.com/g/simPod/DoctrineMoney)
[![GitHub Issues](https://img.shields.io/github/issues/simPod/DoctrineMoney.svg?style=flat-square)](https://github.com/simPod/DoctrineMoney/issues)


## Installation
`composer require simpod/doctrine-money`

## Use
```yaml
doctrine:
    orm:
        mappings:
            Money:
                dir: "%kernel.project_dir%/../vendor/simpod/doctrine-money/src/doctrine/orm"
                prefix: Money
                type: xml
```

Then in entity you can add property of type `Money\Money`:

```php
/**
 * @var Money
 * @ORM\Embedded(class="Money\Money")
 */
private $money;
```
