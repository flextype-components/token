# Token Component

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
