# How to contribute?
Install all requirements and clone the repository.
Create zorza/localsettings.py and there add `DEBUG=True`.
Run the site locally with `python3 manage.py runserver`.
Now you can create a branch for a feature or a bug fix and send a pull request!

# Requirements
* Python 3.4 and later
* Django 2.0
* sassc (for compiling .scss files to .css)

# Python style
* Official Python style guide: https://www.python.org/dev/peps/pep-0008/
* Django code guidelines: https://docs.djangoproject.com/en/dev/internals/contributing/writing-code/coding-style/
* Try to use Django's built-in testing features.

# SCSS and HTML style
Classes should be lowercase with dashes between words, eg. `example-div`.

Make use of HTML5 tags like `<main>`, `<section>`, don't add classes when not necessary.

Don't use inline styling (`<div style="...">`).

Use i18n (`{% load i18n %}` and `{% trans "string to translate" %}`).

In HTML emphasize meaning over presentation,
for example use `<strong>` instead of `<b>`.
Try to make the content accessible for all people, on all devices.

```
$primary-color: #123456;
.class { // space before opening bracket on the same line
	font-family: "Roboto", sans-serif;
	// Prefer double quotes, put space after commas.
	// Don't have lines longer than 80 characters.
	// Use tabs for indentation.

	color: $primary-color;
	&:hover {
		text-decoration: underline;
	}
	// Make use of SCSS features like inheritance and variables.
}
```

# Translations
Extract strings to translate with `python3 manage.py makemessages -l <LANGUAGE_CODE>`.
Then, you can edit the strings in `locale/<LANGUAGE_CODE>`.
To compile the translations, use `python3 manage.py compilemessages`.
Remember to set your `LANGUAGE_CODE` in settings to see the websites in your language.

# Other resources
* How to write git commit messages: https://chris.beams.io/posts/git-commit/
* A git development model: http://nvie.com/posts/a-successful-git-branching-model/
* Check whether your page is readable (text contrast): https://webaim.org/resources/contrastchecker/