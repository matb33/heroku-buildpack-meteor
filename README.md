# Heroku buildpack for meteor, npm compatible

## Usage

```
$ heroku create --stack cedar --buildpack https://github.com/matb33/heroku-buildpack-meteor.git
```

If you get a `! Resource not found` message like I did, then split up the create into two steps (though make sure to `heroku apps:destroy` your previous attempt):

```
$ heroku create --stack cedar
$ heroku config:add BUILDPACK_URL=https://github.com/matb33/heroku-buildpack-meteor.git
```

## Example

See [this project](https://github.com/matb33/heroku-meteor-npm) for an example that leverages this particular fork of Jordan Sissel's awesome meteor buildpack.