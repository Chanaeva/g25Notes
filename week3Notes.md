#DOM
html is parsed into the DOM.
Js can interact with the DOM, html and css are strings that get parsed into the DOM
that is the connection
the DOM is a tree of nodes that can be rendered out to the string. these nodes can have
attributes, this is the css part of it. CSS is parses into the attributes.
##composite selector
get DOM in console by using document.getelement....("")[]  (array index position if needed)
lists of elements are returned as arrays

##querySelector
allows any valid css selector
use queryselector by declaring and assigning it document.queryselector("") then console.log the variable
queryselector is slower than composite selectors  

##creating and destroying
creating and destroying elements are based off of the tree, meaning you must adhere to
process and append or delete according to the tree.

.innerText =
.innerHTML =

Constructor function

function Li(text){
  var li = document.createElement("li");
  var liText = document.createTextNode(text);
  li.appendChild(liText);
  return li;
}

var li1 = new li("Amazing")

var ul = document.createElement("ul");
var pText

#JQUERY
jquery is a library, and external set of code already written.
Two ways to link to project
Download
slower, doesn't require internet to test.
<script src="libs/jquery-2.2.3.min.js></script>"
Link to a CDN
<script src="https://code.jquery.com/jquery-2.2.3.min.js"></script>
faster but must have good internet connection

must be above custom js
 selects $("div").closest(body)
 store a selection var divs = $("div"); stores all divs as an array like selector

toggle - means turning on and off

jquery and DOM events
ready the DOM
add event handler and and pass a function that does what you want.
this in jquery - "this" refers to the context of the outer selection
jquery can chain

#Forms
a way for a user to input information
a form is a group of these, if they are individual then its input not form
 needs a way to send info (i.e. submit button)
 labels
 selection
 input


inputs are self-closing.

##SideNotes
(incrementation)value1 += value2 means value1 = value1 + value2
function f(n){
	var total = 0

for (var i = 0; i <= n; i++) {
	 	total += i
}
	return total
}
f(34)

##API
API (application program interface) is a set of routines, protocols, and tools for building software applications. The API specifies how software components should interact and APIs are used when programming graphical user interface (GUI) components. A good API makes it easier to develop a program by providing all the building blocks. A programmer then puts the blocks together.
Types of APIs
There are many different types of APIs for operating systems, applications or websites. Windows, for example, has many API sets that are used by system hardware and applications — when you copy and paste text from one application to another, it is the API that allows that to work.
Most operating environments, such as MS-Windows, provide an API so that programmers can write applications consistent with the operating environment. Today, APIs are also specified by websites. For example, Amazon or eBay APIs allow developers to use the existing retail infrastructure to create specialized web stores. Third-party software developers also use Web APIs to create software solutions for end-users.

##JSON
alternative to XML, can represent numbers, strings, booleans, null, objects and arrays
to turn object to JSON:
JSON.stringify(object);

to turn JSON to object:
JSON.parse(jsonstring);

functions are not able to be stringified, ie methods. if you try to pass a function to strigify to try to turn it into JSON you will get an empty string.

##XMLHttpRequest

doesn't require page reload to change page
it's an asynchronous call to server
// Create a new XMLHttpRequest object to start
looks like:
var request = new XMLHttpRequest();
// Create a function that is called when the request status has changed
request.onreadystatechange = function () {

  // When the readyState is 4 that means the request has completed
  if (request.readyState == 4 && request.status == 200) {
    console.log(request.responseText);
  }
}
// Tell the XMLHttpRequest where you want it to go and how
request.open('GET', 'https://www.reddit.com/r/starwars.json');    (.json creates JSON)

// Send it off! Good luck little XMLHttpRequest! :D
request.send();

##AJAX
asynchronous is the concept that things can start and finish at different times in
different order

technologies that make up ajax:
html and css
DOM
JSON or XML
XMLHttpRequest
Javascript

JS is single-threaded, it goes down the page, which is why AJAX is important.

jquery AJAX XMLHttpRequest:
$.get("http://www.reddit.com/r/aww.json", function(data) {
// Do something with the data
});

##Eventloop

delays how long before it happens
setTimeout(function (){
  console.log("iago");
}, 100) <- the delay amount


##asynchronous behavior
ways to deal with:
callbacks
.done()
promises
request = function(){
return new Promise(function (resolve, reject){
  do stuff
  })
}
request().then(function(data){
  console.log(data)
  })

States of promise:
pending
resolved
unresolved

rejected is different then unresolved, a rejected promise is still resolved as long as it
returns

Resolved has two different methods: .catch() .then()
.catch() gets it if it's rejected, it's like a safety net
.then() does something with something could be rejected or resolved. It's how you get
data out of the last promise, it helps get data from pending promise jquery's promises
$(document).ready(function(){
  $.get('https://pokeapi.co/api/v2/pokemon/4.json', function(pokemon){
    console.log(pokemon.types[0].type.name);
   $.get(pokemon.types[0].type.url, function(types){
     console.log(types.pokemon);
   })
  })
})


$(document).ready(function(){
  $.get('https://pokeapi.co/api/v2/pokemon/4.json').done or .then (function(pokemon){
    console.log(pokemon.types[0].type.name);
   return $.get(pokemon.types[0].type.url)
  }).done(function(types){
     console.log(types.pokemon);
   }).fail(function(error){
    console.log(error);
  })

##Deployment

Static vs. Dynamic
Dynamic sites use a server-side language or data-base. Generate
Static is just the files that load. write

CDN
shared hosting- shared, no root access, chroot jail, LAMP stack. cheap and reliable but no scalability.
VPS- root access, full control same principle as shared through.
Dedicated server
Platform as a Service PaaS - 'cloud platform'
Infrastructure as a Service - 'cloud platform'


#review --
DOM- document object model, which parses
var articles = document.getElementsbytagname("article"); <- gets you all the articles on the page
articles[2] gets you the third article on the page.
how to change h2:
var h2Text = articles[0].getElementByTagName("h2")
h2Text.innerText="something"
how to make it red:
h2.style.color="red"
Add <p> to h2:
var pText = document.createElement("p")
var text = createTextNode("Iago")
pText.appendChild(text)
h2Text.appendChild(pText)
Get the same in query:
document.querySelector("article:first-child h2")

Respond to Events with Events listeners
Event- interaction with the browser, state change. DOM elements emit events.
var p1 = document.querySelector("p1:nth-child(1)")
p1.addEventListener("click", function(){
  alert("Iago!!")
  })

HTML Forms
<form action="the place you are sending the info to" method="POST">
<label for="looks for id to match with">Iago<input id="what matches with the for label"
type="radio" name="what you group radios with, in general it is what the value is paired with when it is sent(via the post body)" value="what data is sent"></label>
<input type="submit" value="whatever you want on the button">
</form>
to check go into terminal cd into file and run an http-server

this prevents the POST and console.logs the value instead
<script> var form = document.getElementById("form ID");
form.addEventListener("submit", function(event){
  event.preventDefault();
  var dog = $("form ID input[type=radio]:checked").val();
  console.log(dog);

  to send this data:
  $.post("where to send data", function(data){
    do stuff
    })
  });
  </script>

HTTPRequests
Referer- a type of data that can be sent over in the request, massive spelling error that
can't be fixed haha

the real difference between methods besides semantic is nothing, the server can do
whatever it wants with it, but obviously it shouldn't or it's not effective

AJAX

$.ajax({
  url:"where you are getting data from "
  method: "type of post"
  success: function that tells what to do
  })

CORS
white-list is the list of accepted origins

Promises
for asynchronous
wrapping in a promise:
var myDataRequest = new Promise(function(resolve, reject){
$.ajax({
  url:"where you are getting data from "
  method: "type of post"
  success: function(data){
    resolve data;
      }
    });
  });
  var myDataRequest2 = new Promise(function(resolve, reject){
  $.ajax({
    url:"where you are getting data from "
    method: "type of post"
    success: function(data){
      resolve data;
        }
      });
    });
  myDataRequest.then(function(data){
    console.log(data);
    return data;
    }).then(function(data){
      return myDataRequest2;
    }).then(function(data){
      console.log("data 2", data);
      });
    });

Promise.All:
for when the order doesn't matter i.e. when data isn't built on top of each other.
returns a promise still.
Promise.All([
  myDataRequest,
  myDataRequest2
]).then(function(data){
  console.log(data);
});
