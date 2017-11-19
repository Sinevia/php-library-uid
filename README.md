# PHP Library Uid

Class to generate unique identifying strings. Largest attention is paid on human friendly unique identifiers (dated digits)

## Background ##

- Human UUID (32 digits)

  Format: YYYYMMDD-HHMM-SSMM-MMMMRRRRRRRRRRR
  
  2017111908492665991498485465 (with dashes: 20171119-0849-2665-991498485465)
  
- Nano UID (23 digits)

  Format: YYYYMMDD-HHMMSS-MMMMMM-NNN
  
  Examples:
  
  20171119084926659914984 (with dashes: 20171119-084926-659914-984)
  
- Micro UID (20 digits)

  Format: YYYYMMDD-HHMMSS-MMMMMM
  
  Examples:
  
  20171119084926659914 (with dashes: 20171119-084926-659914)
  
- Seconds UID (14 digits)

  Format: YYYYMMDD-HHMMSS
  
  Examples:
  
  20171119084926 (with dashes: 20171119-084926)
  
- Timestamp UID (Unix Time - seconds since 1 Jan 1970)

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
\Sinevia\Uid::humanUuid();       // 32 digits - YYYYMMDD-HHMM-SSMM-MMMMRRRRRRRRRRR
\Sinevia\Uid::nanoUid();         // 23 digits - YYYYMMDD-HHMMSS-MMMMMM-NNN
\Sinevia\Uid::microUid();        // 20 digits - YYYYMMDD-HHMMSS-MMMMMM
\Sinevia\Uid::secUid();          // 14 digits - YYYYMMDD-HHMMSS
\Sinevia\Uid::timestampUid();    // Unix time (seconds since 1 Jan 1970)

\Sinevia\Uid::timestampUidWithRandomPostFix(12); // Unix time + 12 random digits

\Sinevia\Uid::isHumanUid(1);
\Sinevia\Uid::isNanoUid(1);
\Sinevia\Uid::isMicroUid(1);
\Sinevia\Uid::isSecUid(1);
```
