## Puppet Oracle JRE 7

This module will make sure that the following OSes have the Oracle JRE rather than the
collective mis-mash that you get from various OS vendors. (Sometimes that is OK, but
consistency trumps ease in my books.)

* Ubuntu - 32 bit
* Ubuntu - 64 bit
* CentOS - 32 bit
* CentOS - 64 bit
* OSX (tested on 10.8.2)
* Windows (tested on XP)

In theory it will also work on Debian and RedHat, but was not tried.

The module contains the actually installers as downloaded from Oracle. If you use them,
you are implicitly agreeing to the [Oracle Binary Code License Agreement] ](http://www.oracle.com/technetwork/java/javase/terms/license/index.html).

To use in your Puppet manifests, include the _jre7_ module.

```ruby
node default {
  include jre7
}
```

Note: Ubuntu/Debian support was achieved by running the RPM through _alient -- scripts_ and
then updating the version to be Debian compliant using the _dev-revision_ utility that is in
the _devscripts_ package.