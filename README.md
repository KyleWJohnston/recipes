# Recipes 
![CI](https://github.com/vabene1111/recipes/workflows/Continous%20Integration/badge.svg?branch=develop) 
![Stars](https://img.shields.io/github/stars/vabene1111/recipes)
![Forks](https://img.shields.io/github/forks/vabene1111/recipes)
![Docker Pulls](https://img.shields.io/docker/pulls/vabene1111/recipes)

Recipes is a Django application to manage, tag and search recipes using either built-in models or 
external storage providers hosting PDF's, images or other files.

![Preview](docs/preview.png)

[More Screenshots](https://imgur.com/a/V01151p)

## Features

- :package: **Sync** files with Dropbox and Nextcloud (more can easily be added)
- :mag: Powerful **search** with Django's [TrigramSimilarity](https://docs.djangoproject.com/en/3.0/ref/contrib/postgres/search/#trigram-similarity)
- :label: Create and search for **tags**, assign them in batch to all files matching certain filters
- :page_facing_up: **Create recipes** locally within a nice, standardized web interface
- :arrow_down: **Import recipes** from thousands of websites supporting [ld+json or microdata](https://schema.org/Recipe)
- :iphone: Optimized for use on **mobile** devices like phones and tablets
- :shopping_cart: Generate **shopping** lists from recipes
- :calendar: Create a **plan** on what to eat when
- :family: **Share** recipes with friends and comment on them to suggest or remember changes you made
- :heavy_division_sign: Automatically convert decimal units to **fractions** for those who like this
- :whale: Easy setup with **Docker**
- :art: Customize your interface with **themes**
- :envelope: Export and import recipes from other users
- :earth_africa: Localized in many languages thanks to the awesome community
- :heavy_plus_sign: Many more like recipe scaling, image compression, cookbooks, printing views, ...

This application is meant for people with a collection of recipes they want to share with family and friends or simply
store them in a nicely organized way. A basic permission system exists but this application is not meant to be run as 
a public page.
Documentation can be found [here](https://github.com/vabene1111/recipes/wiki).

While this application has been around for a while and is actively used by many (including myself), it is still considered
**beta** software that has a lot of rough edges and unpolished parts.

## Installation
Please refer to the Installation section of the [Documentation](https://vabene1111.github.io/recipes/).

## Contributing

Pull Requests and ideas are welcome, feel free to contribute in any way.

**If you want, feel free to open an issue or pull request to add yourself to the list of awesome contributors.**

### Getting Started
This application is developed using the Django framework for Python. They have excellent 
[documentation](https://www.djangoproject.com/start/) on how to get started, so I will only give you the basics here.

1. Clone this repository wherever you like and install the Python language for your OS (at least version 3.8)
2. Open it in your favorite editor/IDE (e.g. PyCharm)
    1. If you want, create a virutal environment for all your packages.
3. Install all required packages: `pip install -r requirements.txt`
4. Run the migrations: `python manage.py migrate`
5. Start the development server: `python manage.py runserver`

There is **no** need to set any environment variables. By default, a simple sqlite database is used and all settings are
populated from default values.

### Translating

There is a [transifex project](https://www.transifex.com/django-recipes/django-cookbook/) project to enable community driven translations. If you want to contribute a new language or help maintain an already existing one feel free to create a transifex account (using the link above) and request to join the project.

It is also possible to provide the translations directly by creating a new language using `manage.py makemessages -l <language_code> -i venv`. Once finished, simply open a PR with the changed files. 

## License

Beginning with version 0.10.0 the code in this repository is licensed under the [GNU AGPL v3](https://www.gnu.org/licenses/agpl-3.0.de.html) license with an
[common clause](https://commonsclause.com/) selling exception. See [LICENSE.md](https://github.com/vabene1111/recipes/blob/develop/LICENSE.md) for details.

**Reasoning**  
**This software and *all* its features are and will always be free for everyone to use and enjoy.**

The reason for the selling exception is that a significant amount of time was spend over multiple years to develop this software.
A payed hosted version which will be identical in features and code base to the software offered in this repository will
likely be released in the future (including all features needed to sell a hosted version as they might also be useful for personal use).
This will not only benefit me personally but also everyone who self-hosts this software as any profits made trough selling the hosted option
allow me to spend more time developing and improving the software for everyone. Selling exceptions are [approved by Richard Stallman](http://www.gnu.org/philosophy/selling-exceptions.en.html) and the
common clause license is very permissive (see the [FAQ](https://commonsclause.com/)).
