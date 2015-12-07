React Webpack Rails
=======

React Webpack Rails brings power of React and ES6  modules into Rails views through Webpack. Our goal is to make React components (and ReactRouter/Flux libs) fully integrated with Rails. This way Developers boost Rails views with powerful JS. 


## What you get:
* React <-> Rails integration
* JS side helpers - for registering, creating and using React components JS side
* Integrations:
    * alt
    * redux
    * react-router
* Generator that can:
    * initialize project with up-to-date package.json and files structure
    * generate HelloWorld example component
    * create ready to use karma/mocha based testing environment
    * setup eslint and integrate it wich specs 
* Turbolinks support
* Modular integrations/plugins system


Why it's special? Focusing on full Rails integration our redux and alt integration allow developers to share store(s) between components. 

## Instalation


Add this line to your application's Gemfile:

```ruby
gem 'react_webpack_rails'
```

Execute:

    $ bundle

Or install it yourself as:

    $ gem install react_webpack_rails

Then run installation:

    $ rails g react_webpack_rails:install

This will create following files:

```
├── app
│   ├── react
│   │   ├── components
│   │   │   ├── hello-world.jsx
│   │   │   └── hello-world-test.jsx
│   │   └── index.js
│   ├── views
│   │   └── layouts
│   │       └── _react_hot_assets.html.erb
│   └── assets
│       └── javascripts
│           └──react_bundle.js
├── webpack
│   ├── dev.config.js
│   ├── hot-dev.config.js
│   ├── production.config.js
│   └── tests.config.js
├── .babelrc
├── karma.conf.js
├── package.json
└── webpack.config.js
```
You can read more about generator here: [TODO]

Establish the node packages (may take a few moments)

    $ npm install    # you may see warnings to consider updating the provided package.json file with license and repository


And require integration and bundle files in `application.js`

```js
//= require react_integration
//= require react_bundle
```

Now you are ready to go. Checkout Guides to learn how register and use components and more. 

