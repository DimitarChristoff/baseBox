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
IE6, IE7, IE8, IE9, FF3, FF4, Chromium 10, Safari 4.0.4

**note**: IE6, IE7 and IE8 just fade the box up and need CSS ruleset to fall back on,
like (background-image: url(yourgradient.gif); and so forth).

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


Example
-------

[http://jsfiddle.net/dimitar/6creP/](http://jsfiddle.net/dimitar/6creP/)

Events and pointers
-------------------

The following events are raised that youcan reference from your instance

- onOpen - fires when doBox opens.
- onContentLoaded - fires on setHTML method
- onBeforeClose - fires before clean up when closing so you can garbage collect or whatever
- onClose - fires after the box is closed
- onMoving - fires when moving the box starts
- onMoved - fires when stopped moving

`this.modal` stores a pointer to the instance for scripting.
`this.wrap` stores a pointer to the instance for scripting

Extendability
-------------

This also provides baseBox.lightBox - a mini class that extends baseBox as an example and
displays an image in a lightbox style modal. [View extended example](http://jsfiddle.net/dimitar/6creP/36/)

Known issues
------------

- not tested on Opera but should work.