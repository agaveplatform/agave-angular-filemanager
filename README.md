## Agave AngularJS Filemanager

A filemanager dirctive for AngularJS to manage your files in the browser using the Agave Platform. 

#### [Try the DEMO](https://agaveplatform.github.io/angualar-filemanager)
---------

### Features
  - Multilanguage (English / Spanish / Portuguese / French)
  - Multiple templates (List / Icons)
  - Multiple file and directory upload
  - Directory tree navigation
  - Copy, Move, Rename (Interactive UX)
  - Managed file transfers
  - Delete, Edit, Preview, Download
  - Generate disposable public URLs to share data
  - Agave file permissions
  - Mobile support
  - Leverages the Agave AngularJS SDK
---------

### Use in your existing project
**1) Install and use**
```bower install --save angular-filemanager```

**2) Include the dependencies in your project**
```html
<!-- third party -->
  <script src="bower_components/angular/angular.min.js"></script>
  <script src="bower_components/angular-translate/angular-translate.min.js"></script>
  <script src="bower_components/angular-cookies/angular-cookies.min.js"></script>
  <script src="bower_components/jquery/dist/jquery.min.js"></script>
  <script src="bower_components/bootstrap/dist/js/bootstrap.min.js"></script>
  <link rel="stylesheet" href="bower_components/bootswatch/paper/bootstrap.min.css" />

<!-- angular-filemanager -->
  <link rel="stylesheet" href="dist/angular-filemanager.css">
  <script src="dist/angular-filemanager.min.js"></script>
```

**3) Use the angular directive in your HTML**
```html
<angular-filemanager></angular-filemanager>
```

---------

### Using source files instead of minified js
```html
<!-- Uncomment if you need to use raw source code
<!--<script src="src/js/app.js"></script>
<script src="src/js/directives/directives.js"></script>
<script src="src/js/filters/filters.js"></script>
<script src="src/js/providers/config.js"></script>
<script src="src/js/entities/chmod.js"></script>
<script src="src/js/entities/acl.js"></script>
<script src="src/js/entities/item.js"></script>
<script src="src/js/entities/fileitem.js"></script>
<script src="src/js/services/filenavigator.js"></script>
<script src="src/js/services/fileuploader.js"></script>
<script src="src/js/providers/translations.js"></script>
<script src="src/js/controllers/main.js"></script>
<script src="src/js/controllers/selector-controller.js"></script>
<link href="src/css/angular-filemanager.css" rel="stylesheet">
-->

<!-- Comment if you need to use raw source code -->
  <link href="dist/angular-filemanager.css" rel="stylesheet">
  <script src="dist/angular-filemanager.min.js"></script>
<!-- /Comment if you need to use raw source code -->
```

---------

### Extending the configuration file
```html
<script type="text/javascript">
  angular.module('FileManagerApp').config(['fileManagerConfigProvider', function (config) {
    var defaults = config.$get();
    config.set({
      appName: 'github.com/agaveplatform/angular-filemanager',
      allowedActions: angular.extend(defaults.allowedActions, {
        remove: true
      })
    });
  }]);
</script>
```

---------

### Development

Clone and build the project from GitHub

```shell
git clone https://github.com/agaveplatform/agave-angular-filemanager
cd agave-angular-filemanager
npm install
```

To start the demo application locally, run the following 
```shell
gulp localhost
```

The a web server will startup and be available at [http://localhost:9000](). A watch is automatically placed on all 
source files and will hot reload the page when any files are changed. 

By default, the demo points at Agave's public tenant. If you would like to authenticate to another tenant, edit the 
following variables in the `index.html` file.

| Variable name    | Default                      | Description                                                               |
|------------------|------------------------------|---------------------------------------------------------------------------|
| AGAVE_TENANT_ID  | agave.prod                   | ID of the tenant you would like to use.                                   |
| AGAVE_BASE_URL   | https://public.agaveapi.co   | Base URL of the tenant to which you would like to connect.                |
| AGAVE_CLIENT_KEY | xOWNUeaInV_vSauTmYf44wFf6ZEa | Valid client key to use to authenticate using an implicit oauth flow.     |
| AGAVE_AUTH_TOKEN |                              | Valid OAuth access token to use if you would like to skip authentication. |
| AGAVE_SYSTEM_ID  | data.agaveapi.co             | System to which you would like to connect                                 |  
 

### Contribute
To contribute to the project you can simply fork this repo. To build a minified version, you can simply run the Gulp 
task `gulp build`. The minified/uglified files are created in the `dist` folder. 

### Versioning
For transparency into our release cycle and in striving to maintain backward compatibility, angular-filemanager is maintained under [the Semantic Versioning guidelines](http://semver.org/).

### Copyright and license
Code and documentation released under [the MIT license](https://github.com/joni2back/angular-filemanager/blob/master/LICENSE).
