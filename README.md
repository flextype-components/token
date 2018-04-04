# Token Component
![version](https://img.shields.io/badge/version-1.1.0-brightgreen.svg?style=flat-square "Version")
[![MIT License](https://img.shields.io/badge/license-MIT-blue.svg?style=flat-square)](https://github.com/flextype-ccomponents/token/blob/master/LICENSE)

The Token component generate and store a unique token which can be used to help prevent  

Generate token
[CSRF](http://wikipedia.org/wiki/Cross_Site_Request_Forgery) attacks.  
```php
$token = Token::generate();
```

Generate token in the template
```html
<input type="hidden" name="csrf" value="<?php echo Token::generate(); ?>">
```

Check that the given token matches the currently stored security token.  
```php
if (Token::check($token)) {
    // Pass
}
```

## License
See [LICENSE](https://github.com/flextype-components/token/blob/master/LICENSE)
