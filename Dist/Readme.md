*** Udacity FEND Project 5: Website Optimization ***
______________________________________________________
by Oleksii Babenko, June 12, 2017

*** Brief overview ***

The project task is to optimize a provided website with a number of optimization and performance-related issues so that it achieves a target PageSpeed score and runs at 60 frames per second.
___________________________________________________________________________________________________________

*** Steps to launch: ***

1. Clone/download zip. file. Open Index.html in your browser.
2. To view the pizza website open views/pizza.html in your browser.
3. Alternatively, you can view the site on github pages by using the links below.
https://github.com/Bob78Alex/Website_optimization_P5.git
___________________________________________________________________________________________________________

*** Improvements made to Index.html file:***

1. Style.css was inlined into the head of the Index.html document. Atribute [media="print"] was added to the link for print.css.
2. The 'async' atribute was added to all script tags.
3. The HTML compressor tool was used to concatenate and minify file [https://htmlcompressor.com/compressor]
4. All images were resized and compressed using the compressing tool [https://kraken.io/web-interface].
5. Inlined script was placed Placed before the closing [<body>] tag.
__________________________________________________________________________________________________________

*** Improvements made to views/js/main.js for pizza.html file:***

1. Replaced selector [querySelectorAll()] in the changePizzaSizes function with [getElementByClassName()].
2. Replaced all selectors [querySelector()] with [getElementById()].
3. Reduced the number of pizzas generated on page load from 256 to 34 based on the browser window filling.
4. Changed the [querySelector()] call for selecting [movingPizzas1] element to [getElementById()].
5. A new loop was created to iterate through [pizzaContainerLength] to prevent browser from repetitive rendering and repainting.
6. The prorerty [backface-visibility: hidden;] was added to class [.mover] to put each moving pizza to its own layer.
___________________________________________________________________________________________________________

*** Resources used: ***

1. Udacity: https://classroom.udacity.com/nanodegrees/nd001/parts/e87c34bf-a9c0-415f-b007-c2c2d7eead73/modules/273584856175461/lessons/b6026387-b47c-464f-954f-2f807979a066/project.
2. Ghttps://developers.google.com/speed/pagespeed/insights/
3. https://htmlcompressor.com/compressor/
4. Optimizing Google Web Fonts blog post: www.hongkiat.com/blog/optimize-google-webfonts/
5. MDN docs on getElementsByClassName: https://developer.mozilla.org/en-US/docs/Web/API/Document/getElementsByClassName