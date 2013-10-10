# svbheck

svbheck is a responsive theme for [Pelican](http://getpelican.com) which is a modification of the svbhack theme

## Demo

You can see the [theme in action](http://blog.timheckman.net).

## Features

- responsive
- syntax highlighting for pre blocks
- themed support of the following rST admonition classes
	- note
	- important
	- warning
- uses font-awesome icons for Twitter, GitHub, GooglePlus, facebook, and LinkedIn
- supports google analytics
- custom list of links

## Instllation

You want to close the repository to somewhere on your filesystem.

	git clone git@github.com:theckman/pelican-svbheck.git svbheck

Then install the theme in pelican by running the following command:

	pelican-themes -i /path/to/svbheck

Finally, edit the theme directive in the `pelicanconf.py` file to specify the theme:

	…
	THEME = 'svbheck'
	…

You are then set to build the html.

## pelicanconf.py Options

Supports a number of common global variables but patches are welcomed if you need better support.

- `(FACEBOOK|TWITTER|GITHUB|GOOGLEPLUS|LINKEDIN)_URL` the URL to your specific profile

- `GOOGLE_ANALYTICS` your UA-XYZ code

- `USER_LOGO_URL` you don't need to replace the logo placeholder, instead put your logo in content/images/your_logo.png and make this point to `SITEURL + '/static/images/your_logo.png'`

- `DISQUS_SITENAME` set this to enable disqus comments in articles

- `COLLAPSE_COMMENTS` set to `True` to have article comments hidden by default. Clicking on the `comments` link will toggle visibility.

- `TAGLINE` some text rendered right below the logo

- `INTERNET_DEFENSE_LEAGUE` set this to `True` if you want to enable the [Internet Defense League](http://internetdefenseleague.org) code

When developing locally, you may want to set the following variable: `SITEURL = http://localhost:8000`

## Post Metadata

I've also added support for two different metadata fields within the article that will display on the specific artcle page.

- `hackernews` provide a URL to the posted HackerNews comments so people can comment
- `reddit` provide a URL to the posted Reddit comments so people can comment

You can see how to use the file metadata [here.](http://docs.getpelican.com/en/3.1.1/getting_started.html#file-metadata)

## Modifications

- A different Pygmentize theme can be used by editing `./Makefile` and running `make pygments`.

## CSS Notes
While `less` is used for site stlying, the `less.js` code include is commented out in the `base.html` template file. I recommend that you statically compile the CSS using `lessc` after installing the theme and building your site for the first time

## Author

svbheck is authored by Tim Heckman.

## License

Released under MIT License, full details in `LICENSE` file.
