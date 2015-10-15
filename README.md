# command-line-api
Some useful tips for using the Command Line API (in your Inspector).

![Alt text](https://www.dropbox.com/s/13jmctiiuhew1gv/Screenshot%202015-10-13%2013.03.32.png?dl=1 "Screenshot of some functions in use at Chrome Inspector")

### Outline CSS layout
I use this oneliner in cases I for example get an horizontal scrollbar to detect at a glance which element is causing it.

`[].forEach.call($$("*"),function(a){a.style.outline="1px solid #"+(~~(Math.random()*(1<<24))).toString(16)})`

### See all image-URL's of your current page
Often I want to check whether all images are loaded from the right domain, for example after implementing a CDN or after switching the website from the development-environment to the production environment. This snippet let's me check it out in just 5 seconds!

```var pics = $$("img");
for (pic in pics) {
  console.log(pics[pic].src);
}```

### Debugging JavaScript functions
``debug(demoDemo)``

### Monitoring JavaScript functions
``monitor(demoDemo)``

### See all Eventlisteners of a DOM object
``getEventListeners(document.querySelector("#button"))``

### Monitoring events of a DOM object
``monitorEvents(window, "resize");``
``monitorEvents(window, ["scroll", "mousedown"]);``
