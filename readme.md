# Silex Arango Skeleton

Basic skeleton for applications using ArangoDB


### Dependencies
* ArangoDB Driver for PHP  
* Respect Validator
* Twig
* Symfony YAML


### Installation
 Use composer:  

 `composer create-project lvieira/silex-arango-skeleton MyAwesomeProject`  

* Set `public` folder as web root of your application  
* Add your custom configurations to `app.yml`
* Let's code !

### Custom configurations  

On the `app.yml` file you can add your own configurations.  
To disable API prefixes set the configuration `enabled` to `false` under `api` block.

### Controllers

Make sure your Controller is registered on `src/Providers/ControllerServiceProvider.php`  
Example:

```
   $app['foo'] = function (Container $app) {
       return new FooController($app);
   };
```

### Routes

Routes are defined on `routes/routes.yml` file. Be careful while indenting.
To define a route `foo` with action in 'FooController' and method `bar`, just define it as:

```
    foo/:  
        method: get  
        to: foo:bar
```

If you have any route parameters, you can pass it as:

```
    foo/{id}:
        method: get
        to: foo:bar
```
