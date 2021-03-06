OzLockCon Jekyll website
=============

[![Build Status](https://semaphoreci.com/api/v1/klepas/ozlockcon-com/branches/master/badge.svg)](https://semaphoreci.com/klepas/ozlockcon-com)

> Code that builds a static copy of the OzLockCon website.


## Content

* [Configuration](#configuration)
* [Editing content](#editing-content)
* [Dependencies](#dependencies)
* [Building](#building)
* [License](#license)


----------------------------------------------------------------------------------------------------------------------------------------------------------------

## Configuration

Most of the con’s details are tracked in the config file (`_config.yml`), for example:

```yaml
title: OzLockCon
con_year: 2017
con_date: June 3–4th
con_location: Melbourne
email: admin@ozlockcon.com
```

Check out what’s there before you hardcode stuff. (:

These are called in the [templates](https://jekyllrb.com/docs/templates/) like so

```liquid
<a href="mailto:{{ site.email }}">{{ site.email }}</a>
```


**[⬆ back to top](#content)**

----------------------------------------------------------------------------------------------------------------------------------------------------------------

## Editing content

Easiest way is to edit the Markdown files locally.

The site is configured to use the [kramdown Markdown parser](https://kramdown.gettalong.org/syntax.html), which has some pretty nice syntax features.

If you add a new page you will have to manually add it to the navigation include (`_includes/navigation.html`).


**[⬆ back to top](#content)**

----------------------------------------------------------------------------------------------------------------------------------------------------------------

## Dependencies

To build the site locally you will need:

- Ruby 2.3.1 (haven’t tested with later versions; should work fine)
- [Jekyll](https://jekyllrb.com/) `3.3.0` (Ruby-based static site generator)
- [jekyll-assets](https://github.com/jekyll/jekyll-assets) (an asset pipeline)
- [Bourbon](http://bourbon.io/) and [Neat](http://neat.bourbon.io/)

We have automated [CI setup through semaphoreci.com](https://semaphoreci.com/klepas/ozlockcon-com) for the `master` branch.


**[⬆ back to top](#content)**

----------------------------------------------------------------------------------------------------------------------------------------------------------------

## Building

If you need to build the site manually (eg for a manual deploy, or for development):

1. clone the repo
2. set up ruby
3. install dependencies (pulled from `Gemfile`)
4. run/build

(I’m skipping the setup of Ruby here--have fun with that. FWIW, klepas uses [rbenv](https://github.com/rbenv/rbenv).)

```shell
git clone git@github.com:klepas/ozlockcon.com.git
cd ozlockcon.com
bundle install
```

And then either to serve or just build respectively:

```shell
bundle exec jekyll serve
```

```shell
bundle exec jekyll build
```

The generated output files (html/css/…) will reside in the `_site/` folder.


**[⬆ back to top](#content)**

----------------------------------------------------------------------------------------------------------------------------------------------------------------

## License

Code is licensed under [MIT](https://raw.githubusercontent.com/klepas/ozlockcon.com/master/LICENSE).

Content is © 2016– OzLockCon Crew.


**[⬆ back to top](#content)**

# %}
