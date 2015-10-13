# command-line-api
Handy tips for using the Command Line API (in your Inspector)

### Outline CSS layout
`[].forEach.call($$("*"),function(a){a.style.outline="1px solid #"+(~~(Math.random()*(1<<24))).toString(16)})`

### See all image-URL's of your current page
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
