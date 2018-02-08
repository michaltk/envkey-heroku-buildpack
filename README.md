envkey-heroku-buildpack
=======================

A buildpack for loading EnvKey variables before the main buildpack's compilation phase. Useful if you need some of you EnvKey config to be set during compilation--for example, when using NPM private modules, an NPM_TOKEN is required to install dependencies.

