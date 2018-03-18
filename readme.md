# Website des Ferienhauses Schwalbennest Arloff


# How this Website was created

## Install Jekyll and create a default page

https://jekyllrb.com

    rvm gemset use 2.4.1@arloff-plain --create --ruby-version
    gem install jekyll bundler
    jekyll new arloff-website

## Adding Bootstrap

as found on this page: https://simpleit.rocks/how-to-add-bootstrap-4-to-jekyll-the-right-way/

    yarn add bootstrap@4.0.0
    yarn add "jquery@>=3.0.0"

Made config changes as described on above page.

### Adding the Javascript

Still following above doc, but first need to copy the head.html include from the
theme minima which is a gem:

    mkdir \_includes
    cp $(bundle show minima)/\_includes/head.html \_includes/

And added the js includes there.

### Import Bootstrap and use Sass variables

    mkdir assets
    cp $(bundler show minima)/assets/main.scss assets/
