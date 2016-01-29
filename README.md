

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
│       └── index.erb
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

This folder holds our MVC directories.

#### `controllers` directory

This folder holds our application controller file - `application_controller.rb`. Our application controller will be responsible for finding the appropriate views (.erb files with HTML/CSS and embedded Ruby) for each page that the user visits and the correct models (the Ruby code when the applications needs to interact with the database).

#### `models` directory

This folder holds the logic (Ruby code) behind our application. We'll start out with just a `tweet.rb` file with a Tweet class for now. This tweet class will be used to create new instances of tweets and to eventually interact with the database.

#### `views` directory

This directory holds the code that will be displayed in the browser. In a Sinatra app we use .erb files instead of .html files because .erb files allow us to include regular, old HTML tags AND special erb tags which contain Ruby code. We'll start out with just one file `index.erb` which will display the tweets we create.

### `config` directory

This directory holds an `environment.rb` file. We'll be using this file to connect up all the files in our application to the appropriate gems and to each other.

### `public` directory

The `public` directory holds our front-end assets. In the example above, it holds a `css` directory with a stylesheet. Javascript directories and any other front-end assets (like image files) should also be stored in `public`.

### `config.ru` file

A `config.ru` file is necessary if you are using a deployment tool such as `rackup` (the ru stands for rackup) to start up a server. It specifies where to find the application controller so that a new instance of our Sinatra application can be initialized.

### `Gemfile`

This holds a list of all the gems needed to run the application. For example, we'll be using the `pry` gem to test out and debug our application. All of the gems in a Gemfile can be downloaded by running the command `bundle install` from our terminal.






<p data-visibility='hidden'>View <a href='https://learn.co/lessons/hs-advanced-ruby-project-setup' title='Sinatra Application Setup'>Sinatra Application Setup</a> on Learn.co and start learning to code for free.</p>
