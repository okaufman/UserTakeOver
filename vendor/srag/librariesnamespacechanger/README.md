Change the namespace of the libraries on dump-autoload to a plugin specific namespace

### Usage

#### Composer
First add the following to your `composer.json` file:
```json
"require": {
  "srag/librariesnamespacechanger": ">=0.1.0"
},
"scripts": {
    "pre-autoload-dump": "srag\\LibrariesNamespaceChanger\\LibrariesNamespaceChanger::rewriteLibrariesNamespaces"
  }
```

This script will change the namespace of the libraries on dump-autoload to a plugin specific namespace.

For instance the Library `DIC` and the the plugin `HelpMe`, the namespace is `srag\DIC\HelpMe\`.

So you can force to use your libraries classes in the `vendor` folder of your plugin and come not in conflict to other plugins with different library versions and you don't need to adjust your plugins to newer library versions until you run `composer update` on your plugin.

It support the follow libraries:
* [srag/activerecordconfig](https://packagist.org/packages/srag/activerecordconfig)
* [srag/bexiocurl](https://packagist.org/packages/srag/bexiocurl)
* [srag/custominputguis](https://packagist.org/packages/srag/custominputguis)
* [srag/dic](https://packagist.org/packages/srag/dic)
* [srag/jasperreport](https://packagist.org/packages/srag/jasperreport)
* [srag/jiracurl](https://packagist.org/packages/srag/jiracurl)
* [srag/removeplugindataconfirm](https://packagist.org/packages/srag/removeplugindataconfirm)

### Dependencies
* PHP >=5.6
* [composer](https://getcomposer.org)

Please use it for further development!

### Adjustment suggestions
* Adjustment suggestions by pull requests on https://git.studer-raimann.ch/ILIAS/Plugins/LibrariesNamespaceChanger/tree/develop
* Adjustment suggestions which are not yet worked out in detail by Jira tasks under https://jira.studer-raimann.ch/projects/LNAMESPACECHANGER
* Bug reports under https://jira.studer-raimann.ch/projects/LNAMESPACECHANGER
* For external users please send an email to support-custom1@studer-raimann.ch

### Development
If you want development in this library you should install this library like follow:

Start at your ILIAS root directory
```bash
mkdir -p Customizing/global/libraries
cd Customizing/global/libraries
git clone -b develop git@git.studer-raimann.ch:ILIAS/Plugins/LibrariesNamespaceChanger.git LibrariesNamespaceChanger
```
