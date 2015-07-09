# How to install devise

* Add `gem 'devise'` in your `Gemfile`
* Run `bin/rails generate devise:install`
* Copy `config.action_mailer.default_url_options = { host: 'localhost:3000' }`
  in your `development.rb`
* Make sure you add a `root route` in your `routes.rb`
* Add `<p class="notice"><%= notice %></p>` and `<p class="alert"><%= alert %></p>` to your `application.html.erb` or layout file
* Create a devise model if you have not have one yet `bin/rails generate devise
  user`
* Add a `before_filter` in your controller e.g. `before_filter
  :authenticate_user!` will make all your methods need to be signed in to access

### Notes:
* Devise has a `current_user` object that is accessible application wide
* To check if there is a user sign_in call `user_signed_in?`
* `new_user_session_path` for Login
* `new_user_registration_path` for Sign Up
* `destroy_user_session_path` for Sign Out
