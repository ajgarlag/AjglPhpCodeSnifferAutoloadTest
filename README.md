Instructions
============

master branch
-------------

You can test it running:

```
curl -s https://getcomposer.org/installer | php && php composer.phar update --dev && vendor/bin/phing
```

I detected the problem in a box without PEAR installed. In my every day box, I have PHP_CodeSniffer installed with PEAR, so it's on the include_path.
If you do not have php_codesniffer installed in your include path, you will get an error message like this:

```
Execution of target "phpcs" failed for the following reason: /tmp/lala/build.xml:13:41: This task requires the PHP_CodeSniffer package installed and available on the include path

BUILD FAILED                                                                                                                                                                                                         
/tmp/lala/build.xml:13:41: This task requires the PHP_CodeSniffer package installed and available on the include path 
```


composer branch
---------------

You can test it running:

```    
curl -s https://getcomposer.org/installer | php && php composer.phar update --dev && vendor/bin/phing
```

Here you can see everything working.
