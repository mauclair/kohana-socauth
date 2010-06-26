# Kohana 3.* Social Authentication #

## Why this new library ##

Because the existing one from Kohana ([Kohana Auth](http://github.com/kohana/auth)), 
don't let you extend it easily to support different authentication possiblities. With this
library you can write your own drivers and providers.

## Drivers and providers?! ##

Basicly you need ONE driver ([ORM](http://github.com/kohana/orm), [Jelly](http://github.com/jonathangeiger/kohana-jelly), [Sprig](http://github.com/shadowhand/sprig), ...) and ONE (or more) providers. Providers can be everything but 
they all stand for a way of authentication: Email, Username, Facebook, Twitter...

## How to use ##

### Use the included login/logout-controller ###

Soon!
	
### Example of a possible 'Template'-controller ###

Soon!

## How to customize it ##

### Change or write a new driver ###

1. Create a folder `driver` in your application folder
2. Create a file with the name of your driver.
3. Create a class Driver_`NameOfDriver` that extends Socauth_Driver:

    class Provider_CustomDriver extends Socauth_Driver{}

### Change or write a new provider ###

1. Create a folder `provider` in your application folder
2. Create a file with the name of your provider.
3. Create a class Provider_`NameOfProvider` that extends Socauth_Provider:

    class Provider_CustomProvider extends Socauth_Provider
    {
        public function login($params = array()) {}
		public function logout() {}	
    }

4. Two methods are needed at minimum: `login` and `logout` 

## Issues/Bugs/Feature requests ##

Please inform us with the issue tracker on [github](http://github.com/glamorous/kohana-socauth/issues).

## Contribution ##

Feel free to fork the project on [github](http://github.com/glamorous/kohana-socauth) if you want something to add/change on this module.
This can be a new driver or provider or just some stupid bugs that are killing you. If we think it's a good fork, there's a big chance we pull it.

## License ##

This plugin has a [BSD License](http://www.opensource.org/licenses/bsd-license.php). You can find the license in license.txt that is included within the module