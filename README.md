# IDES Receiver
The _IDES Receiver_ is a Single-Page Application that can decrypt and decompress zip files received from the IRS via the IDES gateway.
It does so serverlessly, purely on your local machine in your own browser.
Just
1. Import your PEM-formatted RSA Private key
2. Open the received zip file
3. and generate the XML content

# Supported browsers
* General: modern browser, tested on [firefox](https://www.mozilla.org/en-US/firefox/new/) 41.02
* Generating the XML file: https://github.com/eligrey/FileSaver.js/#supported-browsers

# Under the hood
* [forge.js](https://github.com/digitalbazaar/forge)
* [FileSaver.js](https://github.com/eligrey/FileSaver.js/)
* [Bootstrap](http://getbootstrap.com/)
* [Angular](https://angularjs.org/)
* [JQuery](http://jquery.com/)

# Installation
If it is desired to install the IDES Receiver on your local server:

    make install
    wget http://github.com/Stuk/jszip/zipball/master && unzip master && rm master
    cp Stuk-jszip-82ceacc/dist/jszip.min.js www/js/vendor/jszip.js

# License
Check the [[LICENSE]] file for the full text

# My dev notes: Publishing to gh-pages

First checkout of remote branch locally

    git checkout -b gh-pages origin/gh-pages

Copying files from master to gh-pages

    make publish

If there were any "new" files that were added, a "git add" is needed in "gh-pages" branch followed by a commit and push

Finally, return to master branch

    git checkout master


