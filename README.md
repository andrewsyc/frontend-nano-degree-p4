# frontend-nano-degree-p4

# Website Performance Optimization project

## Comments
    With the continuation of web traffic moving towards the mobile sphere website optimization is an important design
    consideration for all users on devices with smaller screens and more limited bandwidth connections.

### Optimizations Made
  1. index.html
  1. Google Fonts Removed
  2. Minified all CSS and Javascript files.

  3. Some of the css from style.css is inlined, not a best practice but speeds things up.
  4. Removed unused styles.
  5. I made the two javascript scripts async.
  6. Moved Javascript links to the bottom, before </body>.
  1. Optimized images in photoshop
  1. Optimizations to views/js/main.js
  1. Reduced number of fixed pizzas generated.

  1. positions function modified.

    1. Instead of requesting the scrolltop value and dividing by 1250 each time running through the loop I made it it's own variable.
      * This prevents the javascript from requesting the value once for each pizza and dividing that number by 1250 for each pizza. (Originally it was looping 200 times per scrollbar move so 200 times to 1 time)
    1. There are only 5 different phases, so I changed the code to calculate the 5 phases once, and save those phases into an array, which should be easier to pull data out of.


##Project Description

Your challenge, if you wish to accept it (and we sure hope you will), is to optimize this online portfolio for speed! In particular, optimize the critical rendering path and make this page render as quickly as possible by applying the techniques you've picked up in the [Critical Rendering Path course](https://www.udacity.com/course/ud884).

To get started, check out the repository, inspect the code,

### Getting started
    *Note I did not use the first part in this section but rather used a remote server to host files to do Google PageSpeed Insights.
####Part 1: Optimize PageSpeed Insights score for index.html

Some useful tips to help you get started:

1. Check out the repository
1. To inspect the site on your phone, you can run a local server

  ```bash
  $> cd /path/to/your-project-folder
  $> python -m SimpleHTTPServer 8080
  ```

1. Open a browser and visit localhost:8080
1. Download and install [ngrok](https://ngrok.com/) to make your local server accessible remotely.

  ``` bash
  $> cd /path/to/your-project-folder
  $> ngrok 8080
  ```

1. Copy the public URL ngrok gives you and try running it through PageSpeed Insights! Optional: [More on integrating ngrok, Grunt and PageSpeed.](http://www.jamescryer.com/2014/06/12/grunt-pagespeed-and-ngrok-locally-testing/)

Profile, optimize, measure... and then lather, rinse, and repeat. Good luck!

####Part 2: Optimize Frames per Second in pizza.html

To optimize views/pizza.html, you will need to modify views/js/main.js until your frames per second rate is 60 fps or higher. You will find instructive comments in main.js.

You might find the FPS Counter/HUD Display useful in Chrome developer tools described here: [Chrome Dev Tools tips-and-tricks](https://developer.chrome.com/devtools/docs/tips-and-tricks).

### Optimization Tips and Tricks
* [Optimizing Performance](https://developers.google.com/web/fundamentals/performance/ "web performance")
* [Analyzing the Critical Rendering Path](https://developers.google.com/web/fundamentals/performance/critical-rendering-path/analyzing-crp.html "analyzing crp")
* [Optimizing the Critical Rendering Path](https://developers.google.com/web/fundamentals/performance/critical-rendering-path/optimizing-critical-rendering-path.html "optimize the crp!")
* [Avoiding Rendering Blocking CSS](https://developers.google.com/web/fundamentals/performance/critical-rendering-path/render-blocking-css.html "render blocking css")
* [Optimizing JavaScript](https://developers.google.com/web/fundamentals/performance/critical-rendering-path/adding-interactivity-with-javascript.html "javascript")
* [Measuring with Navigation Timing](https://developers.google.com/web/fundamentals/performance/critical-rendering-path/measure-crp.html "nav timing api"). We didn't cover the Navigation Timing API in the first two lessons but it's an incredibly useful tool for automated page profiling. I highly recommend reading.
* <a href="https://developers.google.com/web/fundamentals/performance/optimizing-content-efficiency/eliminate-downloads.html">The fewer the downloads, the better</a>
* <a href="https://developers.google.com/web/fundamentals/performance/optimizing-content-efficiency/optimize-encoding-and-transfer.html">Reduce the size of text</a>
* <a href="https://developers.google.com/web/fundamentals/performance/optimizing-content-efficiency/image-optimization.html">Optimize images</a>
* <a href="https://developers.google.com/web/fundamentals/performance/optimizing-content-efficiency/http-caching.html">HTTP caching</a>


### Tools Used
* Dillinger.io used for updating documentation
 * PhpStorm for IDE and code editing
 * Javascriptcompressor.com for compressing all javascript files.
 * Photoshop for resizing pictures to load more effectively and faster.
 * digitalocean.com for a quick VPS to test speed page (I did not use the localhost environment here).
