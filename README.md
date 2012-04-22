# Middleman on Heroku
### precompiled and served statically

## Usage

    $ git clone http://github.com/indirect/middleman-heroku-app.git mysite
    $ cd mysite
    $ heroku create --stack cedar --buildpack http://github.com/indirect/heroku-buildpack-middleman.git
    $ git push heroku master

The only expectation is that `middleman build` will generate your site into `./build`. That's where Rack::TryStatic will look.

If you want to serve a pretty 404 page, create a file named `404.html` at the root of your site, and it will be served automatically any time Rack::TryStatic can't find a file.