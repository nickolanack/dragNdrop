```text
     _                     __    _
  __| |_ __ __ _  __ _  /\ \ \__| |_ __ ___  _ __
 / _` | '__/ _` |/ _` |/  \/ / _` | '__/ _ \| '_ \
| (_| | | | (_| | (_| / /\  | (_| | | | (_) | |_) |
 \__,_|_|  \__,_|\__, \_\ \/ \__,_|_|  \___/| .__/
                 |___/                      |_|
```

#dragNdrop

easily add drag & drop functionality to dom nodes

##Project Page: Demo & Info

[https://thibaultjanbeyer.github.io/dragNdrop/](https://thibaultjanbeyer.github.io/dragNdrop/)

##Key-Features

- Add draggability to any DOM element
- Add corresponding drop containers
- Callback, Classes and Events available
- Tested on all browsers, IE9 up
- Ease of use
- Lightweight, only 1KB gzipped
- Free & open source under MIT License

##Why?

Because there was nothing this small that does not require jquery out there.


##1. Installation

###easy

Just [download the file](https://github.com/ThibaultJanBeyer/dragNdrop/blob/master/dist/dragNdrop.js) ([minified](https://github.com/ThibaultJanBeyer/dragNdrop/blob/master/dist/dNd.min.js)) and add it to your document:  
`<script src="https://thibaultjanbeyer.github.io/dragNdrop/dNd.min.js"></script>`

###npm

`npm install --save-dev npm-dragndrop`


###bower

`npm install --save-dev dragndrop`

That's it, you're ready to rock!  
Of course you can also just include the function within your code to save a request.


##Usage

Now in your JavaScript you can simply pass elements to the function like so:

**simple**
```javascript
dragNdrop({
  element: document.getElementById('element1'), // draggable element
  dropElements: [ document.getElementById('dropContainer1') ] // dropzone (optional)
});
```
**complete**
```javascript
dragNdrop({
  // element to be dragged (DOM element)
  element: document.getElementById('element1'),
  // custom styles (false / true)
  customStyles: false, // (optional)
  // constraints (false / 'x' / 'y' / DOM element)
  constraints: false, // (optional)
  // drop (false / DOM element)
  dropElements: [ document.getElementById('dropContainer1') ], // (optional)
  // callback(event){}
  callback: function(event) { // (optional)
    // event.element, event.dropped, event.dropElements, event.constraints, event.customStyles
  }
});
```
Check out the [examples page](https://thibaultjanbeyer.github.io/dragNdrop/) for more examples.


##Properties:
| property | type | usage |
|--- |--- |--- |
|element |single DOM element (node) |the element that will be draggable |
|customStyles |false / true (boolean) |when set to true, no styles will be added by the plugin |
|constraints |false / 'x' / 'y' / single DOM element (boolean/ string/ node) |constrain the element: 'x' = element can only be dragged on the x axis. 'y' = element can only be dragged on the y axis. DOM element = element can only be dragged within that container |
|dropElements |false / array of DOM element(s) (node(s)) |one or more drop-elements (where the element can be dropped into) |
|callback |function |a callback function (taking an event object) that gets fired when the element is dropped |

##Callback Event Object:
| event.property | usage |
|--- |--- |
|element |the element that was dropped |
|dropped |false = element was not dropped into a drop-container. [node] = array of dom elements = drop-containers in which the element was dropped |
|customStyles |false / true |
|constraints |false / 'x' / 'y' / single DOM element |
|dropElements |one or more drop-elements (where the element can be dropped into) |

##Events
| name | trigger |
|--- |--- |
|dragNdrop:start |user click/tap the element |
|dragNdrop:drag |user moves the element |
|dragNdrop:stop |user releases the element |
|dragNdrop:dropped |element was dropped into a drop-container |

##Classes
| name | trigger |
|--- |--- |
|.dragNdrop |on every draggable element |
|.dragNdrop--start |on element click |
|.dragNdrop--drag |on element drag |
|.dragNdrop--stop |on element release |
|.dragNdrop--dropped |on successful element drop into container |
|.dragNdrop--dropable |on element that can be dropped into at least one container |
|.dragNdrop__drop--ready |on corresponding dropcontainer when element is dragged |
|.dragNdrop__drop--dropped |on dropcontainer when an element is successfully dropped inside |

###Have Fun!