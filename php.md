# PHP

First off, I'd like to preface this that I don't know PHP and I don't really have a desire to. This mostly exists to find ways around using it.

## Convert PHP files into html

`php index.php > index.html`

## Change all references to `.php` files to `.html`

Run this in the current directory: `LANG=C find ./ -type f -exec sed -i '' 's/.php/.html/g' {} \\;`
