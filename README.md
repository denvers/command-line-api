# command-line-api
Handy tips for using the Command Line API (in your Inspector)

### Outline CSS layout
`[].forEach.call($$("*"),function(a){a.style.outline="1px solid #"+(~~(Math.random()*(1<<24))).toString(16)})`

### Alle images uit je pagina loggen
```var pics = $$("img");
for (pic in pics) {
  console.log(pics[pic].src);
}```

### Functies debuggen
``debug(demoDemo)``

### Functies monitoren
``monitor(demoDemo)``

### Eventlisteners
``getEventListeners(document.querySelector("#button"))``

### Events motniroen
``monitorEvents(window, "resize");``
``monitorEvents(window, ["scroll", "mousedown"]);``
