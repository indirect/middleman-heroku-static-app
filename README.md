# Middleman on Heroku
### precompiled and served statically

## Usage

    $ git clone http://github.com/indirect/middleman-heroku-app.git mysite
    $ cd mysite
    $ heroku create --stack cedar --buildpack http://github.com/indirect/heroku-buildpack-middleman.git
    $ git push heroku master

The only expectation is that `middleman build` will generate your site into `./build`. That's where Rack::TryStatic will look.

You can customize the 404 page that's served if TryStatic can't find a file by editing `source/404.html.erb`.