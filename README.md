# PHP Library SqlDB

Class to generate unique identifying strings

## Background ##

## Installation ##

Add the following to your composer file:

```json
   "repositories": [
        {
            "type": "vcs",
            "url": "https://github.com/sinevia/php-library-uid.git"
        }
    ],
    "require": {
        "sinevia/php-library-uid": "dev-master"
    },
```

## Usage ##


```php
\Sinevia\Uid::humanUuid();       // 32 digits - 12 random digits
\Sinevia\Uid::nanoUid();         // 23 digits - YYYYMMDD-HHMMSS-MMMMMM-NNN
\Sinevia\Uid::microUid();        // 20 digits - YYYYMMDD-HHMMSS-MMMMMM
\Sinevia\Uid::secUid();          // 14 digits - YYYYMMDD-HHMMSS
\Sinevia\Uid::timestampUid();    // Unix time (seconds since 1 Jan 1970)
\Sinevia\Uid::timestampUidWithRandomPostFix(12);
\Sinevia\Uid::isMicroUid(1);
```
