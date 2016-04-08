# command-line-api
Some useful tips for using the Command Line API (in your Inspector).

![Alt text](https://www.dropbox.com/s/13jmctiiuhew1gv/Screenshot%202015-10-13%2013.03.32.png?dl=1 "Screenshot of some functions in use at Chrome Inspector")

### Outline CSS layout
I use this oneliner in cases I for example get an horizontal scrollbar to detect at a glance which element is causing it.

```javascript
[].forEach.call($$("*"),function(a){a.style.outline="1px solid #"+(~~(Math.random()*(1<<24))).toString(16)})
```

### See all image-URL's of your current page
Often I want to check whether all images are loaded from the right domain, for example after implementing a CDN or after switching the website from the development-environment to the production environment. This snippet let's me check it out in just 5 seconds!

```javascript
var pics = $$("img");  
for (pic in pics) {  
  console.log(pics[pic].src);  
}  
```

### Debugging JavaScript functions
One of my favorites. Of course you can add breakpoints right into the Developer Tools, or add the ``debugger;`` command right into your JavaScript function, but I love the console. If you know your JavaScript function to debug, just add this snippet in the console and trigger the function via your website/GUI. Lovely function!

```javascript
debug(demoDemo)
```

### Monitoring JavaScript functions
Sometimes I want to check how often a function is called, and in some cases I want to know which arguments are passed to the function. Use this ``monitor`` function to get all this information!

```javascript
monitor(demoDemo)
```

Note: These functions are not usable if you scoped your functions, for example using an anonymous function like 

```javascript
(function() {  
// your code  
}();  
```

### See all Eventlisteners of a DOM object
Oh my god, how often I needed this... Get all attached event listeners to your DOM object. Just use ``getEventListeners`` and pass the targeted DOM object to see all attached listeners right into your console!

```javascript
getEventListeners(document.querySelector("#button"))
```

### Monitoring events of a DOM object
``monitorEvents(window, "resize")``  
``monitorEvents(window, ["scroll", "mousedown"])``

### Get in touch
You can find me at Twitter: [@webvakker](http://www.twitter.com/webvakker/)
