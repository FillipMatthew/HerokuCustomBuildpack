# Heroku Buildpack: Executable

This is a custom Heroku buildpack for an executable.

## Getting Started

(These instructions assume you have the
[heroku tools](https://toolbelt.heroku.com/) and
[git](http://git-scm.com/) installed, and that you have a heroku
account.)

Create a Heroku app, and specify this buildpack.

```
heroku config:add BUILDPACK_URL=https://github.com/FillipMatthew/HerokuCustomBuildpack.git
```

Push the app to Heroku. Learn more about [deploying to Heroku with git][deploy].

```bash
$> git push heroku master
```

## Configuration

### Specifying the script

Create the file `Procfile` in the root of your package to define the file to run when the application starts. We
recommend to put the server script into your application's `bin/` directory.

The sample app's `Procfile` looks like:

```
web: bin/server
```

This project was started from Ilya Grigorik's buildpack. https://github.com/igrigorik/heroku-buildpack-dart.git

## License

The MIT License - Copyright (c) 2022 Matthew Hale
