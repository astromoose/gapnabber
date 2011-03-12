#GapNabber#


*So that* I can scrape a useful catalogue of product *ata from gap.com with colour and size information
*As a* Gapnabbing chap
*I can* run a script passing in a url and produce portable, serialised data expressing the above catalogue

## Dependencies ##

ruby
jruby

*Gems*
celerity
yaml

## Usage ##
Usage: ./gapnabber [options]
    -u, --url U                      Nab from the specified url
    -h, --help                       Display this screen

## What works ##
* Parses a url, goes to it and grabs a list of urls from the page - seems to work on all GAP category pages
* Gets Product name and id for a product, and the list of colours/prices it is available in
* Serialises data to yaml

## What does not work ##
* Javascript, which means no sizes. Or size chart popup.

## TODO
* Fork product data loop for speed - this would need some abstraction work, jruby does not support fork (unsafe, apparently)
* Tidy up yaml, newlines all over the place and special characters galore
* Add a 'quiet' option to suppress the browsing output
