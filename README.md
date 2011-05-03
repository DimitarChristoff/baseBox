baseBox
=======

![Screenshot](http://fragged.org/img/baseBoxSShot.jpg)

A MooTools 1.3 modal box class which works fine with CSS3 features like:
 - gradients
 - border-radius
 - transition: scale
 - box-shadow - inset and normal
 - rgba
 - text-shadow
 - graceful degradation for older browsers via CSS only
 - supports -ms-transform, -moz-transform and -webkit-transform through Fx.Morph

Tested on
---------
IE6*, IE7*, IE8*, IE9**, FF3, FF4, Chromium 10, Safari 4.0.4


How to use
----------

Get the required MooTools 1.3 core and build MooTools-more with Element.delegation and Drag.Move

Within your **domready** or **load** callback function, create an instance with whatever options suit you:

    var box = new baseBox({
        element: this.wrap,
        warpClass: "baseBox baseBox2",
        width: 300,
        height: 100,
        centered: false,
        offsets: {
            x: 140,
            y: 100
        },
        modal: {
            enabled: false
        }
    });

    // open it.
    box.doBox("<h2>sub window</h2>", "<div class='moto shadowy'>this is a sub window from main</div><center><img class='closeThis cur' src='http://www.webtogs.co.uk/img/modal_close2.png' /></center>");

Known issues
------------

- not tested on Opera