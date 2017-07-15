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

rails g controller Pages home about contact
to check for errors enter raise into controller method,
also in view inspect instance variable using <%= @posts.inspect %>

git status && git add . && git commit -m ''
git push

## create model
git checkout -b model-generator
rails g model Skill title percent:integer
rake db:migrate
rails c
Skill.create!(title: "Rails", percent: 60) // ! so doesn't fail silently
Skill.create!(title: "HTML", percent: 90)
Skill.create!(title: "CSS3", percent: 80)
Skill.all
In pages controller for home action, add blog and skills all records,
then in home view add skills inspect with headings. Call blog and skills inside pages controller
> to merge branches there are 2 ways

Best & quickest way if working on own
* git add and commit
* git checkout master
* git merge model-generator
* git push

In a team use this way
* git add .
* git commit -m ''
* git push origin new-branch-name // new branch will be on github
* to merge, beside new branch name, compare and pull requests
* leave comment with markdown if needed
* create pull request
* merge pull request
* confirm merge
* locally use git checkout master
* git pull

