# Hello Devise

This repository for hello devise rails gem. A very basic steps to configure devise rails gem.

* Create a rails project

`rails _5.0.2_ new hello_devise --database postgresql`

after that

`cd hello_devise/`

* add `devise` gem in Gemfile

`gem 'devise'`

* do `bundle`

* create database

`bin/rake db:create`

* Install `devise`

`bin/rails g devise:install`

After that you will see following on screen.
```
$ bin/rails g devise:install
      create  config/initializers/devise.rb
      create  config/locales/devise.en.yml
===============================================================================

Some setup you must do manually if you haven't yet:

  1. Ensure you have defined default url options in your environments files. Here
     is an example of default_url_options appropriate for a development environment
     in config/environments/development.rb:

       config.action_mailer.default_url_options = { host: 'localhost', port: 3000 }

     In production, :host should be set to the actual host of your application.

  2. Ensure you have defined root_url to *something* in your config/routes.rb.
     For example:

       root to: "home#index"

  3. Ensure you have flash messages in app/views/layouts/application.html.erb.
     For example:

       <p class="notice"><%= notice %></p>
       <p class="alert"><%= alert %></p>

  4. You can copy Devise views (for customization) to your app by running:

       rails g devise:views

===============================================================================

$
```
* Create a devise user
  `$ bin/rails g devise user `
* do migrate   
  `$ bin/rake db:migrate `

* Now start server `bin/rails s -p 9999` and access page with following urls.

```
* Sign Up - http://localhost:9999/users/sign_up
* Sign In - http://localhost:9999/users/sign_in
* Forget Password - http://localhost:9999/users/password/new
```
