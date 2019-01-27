# API Only JWT Authentication using Devise & Knock

This is a sample Rails application that uses [Devise](https://github.com/plataformatec/devise) (a popular authentication solution) and [Knock](https://github.com/nsarno/knock) (A JWT handler gem).

_Learn more about JWTs [here](https://jwt.io)_

## Tutorial

1. Create a rails application in API only mode.

```Bash
$ rails new jwt_test --api
```

2. Add the required gems to the Gemfile

```Ruby
  gem 'devise'
  gem 'knock'
```
