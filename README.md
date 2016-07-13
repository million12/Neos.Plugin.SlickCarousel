# M12.SlickCarousel - Slick carousel for Neos CMS

[Slick Carousel](https://github.com/kenwheeler/slick) node type
for [Neos CMS](https://www.neos.io/).


## Installation

* Install this Neos plugin via composer:  
```
composer require m12/neos-nodetype-slickcarousel:dev-master
```

* Install Slick code in your site package. Refer to 
  [Slick](https://github.com/kenwheeler/slick) documentation for details,
  you will need to include `slick.js`, `slick.css` and perhaps 
  `slick-theme.css` to your page.

* Add the following code to the end of BODY tag:
```
var slickEl = $('.m12-slickcarousel-slick');

$(slickEl).on('init', function(event, slick) {
    // Support non-standard 'nextOnClick' option:
    if (slick.slickGetOption('nextOnClick')) {
        $(slick.$slider).on('click', function() {
            slick.slickNext();
        });
    }
});

// Initialise Slick
$(slickEl).slick();
```

Also see the [Pb.Site](https://github.com/million12/Pb.Site) site package
for a complete example of how to install it with npm/gulp.


## Author(s)

* Marcin Ryzycki marcin@m12.io  

Licensed under: The MIT License (MIT)

**Sponsored by** [PrototypeBrewery.io - the new prototyping tool](http://prototypebrewery.io/) 
for building fully interactive prototypes of your website or web app. Built on top of 
Neos CMS and Zurb Foundation framework.
