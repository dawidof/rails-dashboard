# Rails Dashboard

This application is dev-tool for rails, to improve your rails log.


![demo](https://raw.githubusercontent.com/y-takey/rails-dashboard/master/demo/demo.gif)

##### Breakdown View

![demo](https://raw.githubusercontent.com/y-takey/rails-dashboard/master/demo/img-0-breakdown.png)

##### Params View

![demo](https://raw.githubusercontent.com/y-takey/rails-dashboard/master/demo/img-1-param.png)

##### ActiveRecords View

![demo](https://raw.githubusercontent.com/y-takey/rails-dashboard/master/demo/img-2-sql-2.png)

![demo](https://raw.githubusercontent.com/y-takey/rails-dashboard/master/demo/img-2-sql-1.png)

##### Renderings View

![demo](https://raw.githubusercontent.com/y-takey/rails-dashboard/master/demo/img-3-view.png)

##### (Raw) Log View

![demo](https://raw.githubusercontent.com/y-takey/rails-dashboard/master/demo/img-4-log.png)


## Usage

```
$ npm install -g rails-dashboard
$ cd your/rails/project
$ rails-dashboard bin/rails s

# If you use npm 5.2 or higher
$ cd your/rails/project
$ npx rails-dashboard bin/rails s
```

and go to 'http://localhost:3000', then any operate.

## Keymap

key | desc
---- | ----
<kbd>j</kbd> or <kbd>↓</kbd> | move down main-view by 1 row
<kbd>k</kbd> or <kbd>↑</kbd> | move up main-view by 1 row
<kbd>space</kbd> | move down main-view by 1 page
<kbd>shift</kbd> + <kbd>space</kbd> | move up main-view by 1 page
<kbd>g</kbd> | move to top
<kbd>shift</kbd> + <kbd>g</kbd> | move to bottom
<kbd>shift</kbd> + <kbd>j</kbd> | move down sub-view(currently [Log] tab only) by 1 row
<kbd>shift</kbd> + <kbd>k</kbd> | move up sub-view(currently [Log] tab only) by 1 row
<kbd>enter</kbd> | show detail about selected row
<kbd>escape</kbd> | hide detail
<kbd>b</kbd> | show detail with Breakdown tab
<kbd>p</kbd> | show detail with Params tab
<kbd>a</kbd> | show detail with ActiveRecord tab
<kbd>r</kbd> | show detail with Rendering tab
<kbd>l</kbd> | show detail with Log tab

## Disclaimer

* supported terminal application is Terminal.app, iTerm2.app and [Hyper](https://hyper.is/) on Mac OS. (maybe works fine on Windows and Linux)
* recommended terminal window size is 100 cols * 30 rows higher.
* current supported Rails is version 5.1 and using Puma. but if there is no difference in format of the log, maybe works fine. If don't works fine, send the log to me please.


## Troubleshooting

### Not working to scroll in (long) log subview.

#### iTerm2.app

Try to run following command, and restart iTerm2.

`$ defaults write com.googlecode.iterm2 AlternateMouseScroll -bool true`

FYI: https://stackoverflow.com/a/24695541

#### Terminal.app

You'll need to allow mouse reporting. on menu [View] → [Allow Mouse Reporting].

## Inspired by

* [RailsPanel](https://github.com/dejan/rails_panel) : RailsPanel is a Chrome extension for Rails development that will end your tailing of development.log
* [webpack-dashboard](https://github.com/FormidableLabs/webpack-dashboard) : A CLI dashboard for your webpack dev server.
* [Tig](https://github.com/jonas/tig) : Tig is an ncurses-based text-mode interface for git.

Thanks!

## Contributing

Pull requests and issues are always welcome.

For bugs and feature requests, [please create an issue](https://github.com/y-takey/rails-dashboard/issues).

1. Fork it!
2. Create your feature branch: `git checkout -b my-new-feature`
3. Commit your changes: `git commit -am 'Add some feature'`
4. Push to the branch: `git push origin my-new-feature`
5. Submit a pull request!

## Development

### (optional) Setup Rails app

1. clone [the Rails repository](https://github.com/y-takey/dmy-rails). `$ git clone https://github.com/y-takey/dmy-rails`
2. setup. `$ cd dmy-rails && bundle && bin/rails db:migrate`

### Setup

1. clone this repository. `$ git clone https://github.com/y-takey/rails-dashboard.git`
1. npm install. `$ cd rails-dashboard && yarn install # or npm install`

### Run

```
$ cd your/rails/project/path  # e.g. cd dmy-rails
$ NODE_ENV=dev ../rails-dashboard/node_modules/.bin/babel-node ../rails-dashboard/bin/rails-dashboard.js bin/rails s

# or to generate dummy request, use this
$ NODE_ENV=dmy ../rails-dashboard/node_modules/.bin/babel-node ../rails-dashboard/bin/rails-dashboard.js bin/rails s
```
