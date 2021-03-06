silexXliffEditor, a simple Silex based Xliff Editor
===================================================

Installation
------------

* After cloning the repo you'll have to update the submodules

```
git submodule update --init
```

* Sample Apache Vhost

```
<VirtualHost *:80>
  ServerName  silexXliffEditor.lan
  DocumentRoot "/PATH/TO/silexXliffEditor/web"
  DirectoryIndex index.php

  <Directory "/PATH/TO/silexXliffEditor/web">
    RewriteEngine On
    RewriteCond %{REQUEST_FILENAME} !-f
    RewriteRule ^(.*)$ index.php [QSA,L]
  </Directory>

</VirtualHost>
```

* Update the src/app.yml to your needs (it's probably a good idea to add it to your .gitignore file)

JS Libraries used
-----------------

* jquery.autogrow : https://github.com/jerryluk/jquery.autogrow.git
* jquery.jkey.js : https://github.com/OscarGodson/jKey.git
* jquery.simplemodal.1.4.1.js : http://code.google.com/p/simplemodal/downloads/list
* jquery.sort.js : https://github.com/jamespadolsey/jQuery-Plugins
* jquery.translate.js : http://code.google.com/p/jquery-translate

Similar Project
---------------

* Pootle : http://translate.sourceforge.net/wiki/ (only supports Gettext format)
** ex : http://translate.hootsuite.com/fr/HootSuite/fr.po/translate/
* myGengo : http://mygengo.com/translation-services/string/

TODO / COULD DO
---------------

* allow multiple directories in app.yml
* update jquery-translate to use "Microsoft Translator service" instead of "Google Translate API"
* user Symfony2 forms!
* improve Twig integration
* support Gettext .po file editing
* support translation revision (GIT based?)
* better support user/group (proper ACL)
* implement/fix logout