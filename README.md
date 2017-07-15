# README
This README would normally document whatever steps are necessary to get the
application up and running.

Things you may want to cover:

* Ruby version
* System dependencies
* Configuration
* Database creation
* Database initialization
* How to run the test suite
* Services (job queues, cache servers, search engines, etc.)
* Deployment instructions
> this is a blockquote

- bullet
- points

```
  code block
  def
  end
```

## Initial setup
rails new . -T --database=postgresql
rake db:create
rake/rails db:migrate
rails g scaffold Blog title body:text
rails db:migrate
git rm . -r --cached
test that secrets aren't showing up on git status

## steps for creating branches
git checkout -b controller-generator
git branch
make changes
git status && git add . && git commit -m ''
git push origin controller-generator
in github merge commit and locally do git pull

rails g controller Pages home about contact
to check for errors enter raise into controller method,
also in view inspect instance variable using <%= @posts.inspect %>

