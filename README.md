## Installation
```
composer require devinow/id
```
## Usage

### Creating an instance

```php
$generator = new \Devinow\Ids\Id();
```

### Encoding and decoding IDs

```php
$generator->encode(6); // => "43Vht7"
$generator->decode('43Vht7'); // => 6
```

### Shortening a number without obfuscating it

```php
$generator->shorten(3141592); // => "vJST"
$generator->unshorten("vJST"); // => 3141592
```

### Obfuscating a number without shortening it

```php
$generator->obfuscate(42); // => 958870139
$generator->deobfuscate(958870139); // => 42
```