envkey-heroku-buildpack
=======================

A buildpack for loading EnvKey variables before the main buildpack's compilation phase. Useful if you need some of you EnvKey config to be set during compilation--for example, when using NPM private modules, an NPM_TOKEN is required to install dependencies.

Requires that a valid ENVKEY is set as a heroku config var.

Usage
-----

Example usage:

    $ heroku buildpacks:add --index 1 https://github.com/envkey/envkey-heroku-buildpack

    $ heroku config:set ENVKEY=...

    $ git push heroku master
    ...
    -----> EnvKey-enabled app detected
    -----> Attempting to load, decrypt, and export EnvKey variables
           ENVKEY config var is set
           Downloading envkey-source 1.1.7 from https://github.com/envkey/envkey-source/releases/download/v1.1.7/envkey-source_1.1.7_linux_amd64.tar.gz
           EnvKey variables exported
