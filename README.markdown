# Typeajax

A basic, easily extended plugin for quickly creating elegant AJAX autocompletes any form text input built on top of [Bootstrap Typead](http://twitter.github.io/bootstrap/javascript.html#typeahead).

The main difference of typeajax is the feedback on every stage of the search, which basically all other autocomplete plugins does not provide natively.

Typeajax provides a loading feedback while the user is typing, another feedback when no items are found and another feedback when something wrong happens on the server, i.e.: 401, 403, 500, etc.

## Usage

``` html
<input type="text" id="person" data-typeahead-url="/people/typeahead">
```

You may prefer to use the item id instead of parsing the value on the server (recommended). If you want it, you just need to place a hidden field before the autocomplete input and it will be filled automatically:

``` html
<input type="hidden" id="person_id">
<input type="text" id="person" data-typeahead-url="/people/typeahead">
```

In both cases, you need to call the plugin:

``` javascript
$("#person").typeajax();
```

It's on the to-do list to not need this javascript call but it's required for now.

## Dependencies

* jQuery
* Bootstrap
* Underscore

## TODO

* Support markup API without writing a single line of JavaScript
* Remove undescore dependency since we already depend on jQuery and Bootstrap itself
* Basic i18n support for feedback messages
* Automated tests :flushed:

## License

MIT License. Copyright 2013 Hite. http://hite.com.br
