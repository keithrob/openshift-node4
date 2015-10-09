<p align="center"><img src="https://cloud.githubusercontent.com/assets/129737/10396435/6f2cc8ee-6e70-11e5-8907-5b259b478c91.png"/></p>


# [node.js v4](https://nodejs.org/) cartridge for [OpenShift](https://www.openshift.com/)

## Usage

`rhc create-app <app name> https://raw.githubusercontent.com/connyay/openshift-node4/master/metadata/manifest.yml`


What this cartridge provides out of the box
---
1. **node.js** ([latest stable](http://semver.io/node/stable) currently 4.1.1)
2. **npm** (latest stable currently 2.14.2)
3. **[grunt](https://www.npmjs.com/package/grunt-cli)**
4. **[gulp](https://www.npmjs.com/package/gulp)**
5. **[forever](https://www.npmjs.com/package/forever)**
6. **[bower](https://www.npmjs.com/package/bower)**

What this cartridge does out of the box
---
1. Installs node.js v4
2. Installs grunt, gulp, bower, and forever globally. User can install more via `$OPENSHIFT_NPM_GLOBALS`.
3. Installs Ruby compass.  User can install more Gems via `$OPENSHIFT_RUBY_GEMS`
3. Allows the user to manually install required dependencies (in a `build` [action_hook](http://openshift.github.io/documentation/oo_user_guide.html#action-hooks)). An example of this can be found [here](template/.openshift/action_hooks/build)
4. Runs `npm start` if `package.json` is found in repo directory (log is written to `$OPENSHIFT_NODE4_LOG_DIR`)

