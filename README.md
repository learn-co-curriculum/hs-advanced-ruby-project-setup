---
tags: kids, advanced
languages: ruby, html, css
---

## Sinatra Application Setup

We will be using the Sinatra web framework to create a web application. Practice your command line skills by building out the MVC file structure below with mkdir and touch. We've also included a quick summary of what each of those directories and files is used for at the bottom of the page. 

```bash
project-fwitter
├── app
│   ├── controllers
│   │   └── application_controller.rb
│   ├── models
│   │   └── tweet.rb
│   └── views
│       └── tweets.erb
├── config
│   └── environment.rb
├── public
│   └── css
│       └── style.css
├── config.ru
├── Gemfile
└── README.md
```

### `app` directory

### `models` directory

This folder holds the logic behind your program. If you were building facebook you would save your user.rb file with a User class in this directory.

#### `public` directory

The `public` directory holds our front-end assets. In the example above, it holds a `stylesheets` directory where all of our stylesheets are located. Javascript directories and any other front-end assets (like image files) would be stored in `public` as well.

### `views` directory
In a Sinatra app we use .erb files instead of .html files because .erb files allow us to include regular, old HTML tags AND special erb tags which contain Ruby code. 

#### `application_controller.rb` file

Our `application_controller.rb` inherits from `Sinatra::Base`, which means it inherits all kinds of functionality from the Sinatra gem. This includes the ability to set up routes that correspond to URLs and to display the appropriate .erb files (with HTML/CSS and embedded Ruby) in the browser. 

#### `config.ru` file

A `config.ru` file is necessary if you are using a deployment tool such as `shotgun` (see `Gemfile`). It specifies to our app handler what files should be run in order to initialize a new instance of our Sinatra application.

#### `Gemfile`

This holds a list of all the gems needed to run the application. For example, we need the `shotgun` gem to get a server started on our computer. All of the gems in a Gemfile can be downloaded by running the command `bundle install` from our terminal.





