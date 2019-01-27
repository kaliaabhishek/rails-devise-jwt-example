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

Then run the `$ bundle install` command to add these gems to your application

3. Set up Devise

```Bash
  $ rails g devise:install
```

Follow the instruction prompted ny the generator to finish setting up Devise

4. Set up Knock

```Bash
 $ rails g knock:install
```

This will add a `knock.rb` initializer to the application which can be used to modify default JWT setings.

5. Generate Devise model `User`

```Bash
 $ rails g devise User
```

This will add the files necessary to set up User as the authentication model. Complete the process by running `$ rails db:migrate` to create the User table in the database.

6. Generate a Knock token controller to handle authentication requests

```Bash
 $ rails g knock:token_controller User
```

This will add a `user_token_controller.rb` to the `app/controllers/` directory and also create a POST route to handle authentication requests. Notice that we are generating a token controller for the User model generated in the previous step.
