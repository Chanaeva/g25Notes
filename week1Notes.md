#CLI
package = program
https://en.wikipedia.org/wiki/Package_manager

command line is used to quickly easily use programs that can be combined and what not…

brew is a package manager

##Paths
absolute path is the path to a file from anywhere, a forward slash ( / ) specifies root meaning it’s an absolute path
relative path is the path to a file from where you are in a directory

##Random
.  = current directory
.. = up directory
grep “ “ =  finder
cp = copy
history = tells all history
-r = recursive
touch = creates files by updating time stamp, updates time stamp
more = page through
less = because less is more, file reader

##Piping
introduced in unix
takes the output of one package to be the input of another package ( | )
">  output"
">>  append"
""<  input"

Unix philosophy: do one thing and do it well. then combinations create sophisticated programs.

chains = combining of tasks with && and ;
&& =  after first success “then and”
; = “and” doesn’t require first success

##Permissions
Permissions reference treehouse. first of 7 permissions is the directory, file type.
chmod = octal representation, change permissions, also takes in “u+x” stuff
chown = change ownership
sudo = makes root user, has all power
sudo su = makes root user for session

command line murder mystery for more practice

#Git and GitHub

git init- initialize repository into the an empty directory

git add- takes untracked files added in the repository and starts the process of them being tacked.

git commit- makes a save of the files (at this point in time you have a local repository)

git status- tells me repository files status
 git log- shows all previous commits

git push [origin] [master]
git remote -v = tells you all your places your pushing to
git remote add origin = tell the url of github or wherever
(pushing is the process of taking a local repository and putting it on github)

#HTML
is a tree structure, a tree structure starts with one root and is the parent child structure/relationship that can continue with no end.
character whatsamahozits for special html characters so that they can be read as not html.
less than symbol:
&ls;
greater than symbol:
&gt;

& starts

between tags is called content

##element vs tag
tag is a tag
element is an object that comes from the browser reading the html.

user style is the default style given to elements by the browser

##Random
(cmd + opt + i) brings up dev tools
(cmd + opt +u)

html 5 document type is <!doctype html> no caps needed

title tag sets the title for the browser and is what is displayed in searches and bookmarks

head is meta data not shown on actual webpage to user
body is everything that you have control over

meta char set is not needed for up to date html 5 but required for older versions of html

attributes are things on tags in the form of
<p attribute=“value”>

self-closing = closing itself, meaning it can’t have children

( man.io ) shortcut for mozilla for what you have going on.

##Semantic HTML
separation of discernment of concerns
SEO
Accessibility
Readability
Consumability

(cmd + opt + f) = make full screen
indenting = shift tab and command with brackets

#CSS

css = cascading style sheet
cascading = things follow down the arrangement so styles are applied in a way
that if the body has a color everything else on the same or lesser priority will have
what the body has.

advantages = speed, maintainability, accessibility, can apply one sheet to many
pages, and bandwidth

##Connecting css
Inline style sheet is css right in html tags, highest priority but not best practice.
Internal style sheet uses style tags in html, again not best practice.
External style sheet uses a link to a separate sheet containing all styles, best
practice.
  to connect external style sheet use a link in the head of html:
  <link rel="stylesheet" href="style.css">

##random
In in atom to quick start an html doc type html then hit tab
rel stands for relationship

##Selectors
types: element, class, id  
priority list highest first: id, class, element
Ids are only used once on a page but you can have multiple different id
Wildcard selector is * and it affects everything on the page

##Combinators
Descendant selector targets and element that is a child at any point in time of the
parent element ex:
    div p {}
Child selector targets only a direct child of the parent element ex:
    div > p {}
Adjacent sibling selector targets adjacent FOLLOWING siblings of the selector but
not the
selector ex:
    div + p {}
General sibling selector targets all the siblings of the selector except the
selector
ex:
  div ~ p {}

Group Selectors are separated with ,

##Descendant vs child
Descendant can be a grandchild

##Properties
color is a font property.

color picker hexdecimal, predefined colors, rgb(), and vec()

this is a serif-font

Sizes: pixels, em, rem, %
Em = relative way to define sizes
Rem = root em, relative to the root defaults
relative sizes are good to use for scalability

short-hand properties are properties that allow you to define several values within
one short-hand property

##Inline and Block elements
Block elements always start on a new line
Inline elements take up whatever space they can such as next to a block or other
inline elements.

##Box model
every element in the DOM can be represented by a box, it's how it's defined by
size, the element is not just it's content.

Box sizing is a short-hand, that changes the default box model.

Padding is the space between the content and where it's border would be.
Margin is the space the element takes outside the border.

##Layout
Floats = is a concept from the printing world, gives to the flow of the page,
allows the elements to wrap around block elements, floated

clear
clear: both; = starts element on new line  

##Specificity
Specificity is defined as 1 and more Specificity is added by additional 0s
separated by commas more 0s = greater weight which is greater Specificity.
Inline styles have a default of highest Specificity.
Directly targeted elements always take precedence over inherited rules.  

##Normalize or Reset
Normalize renders all elements more consistently and in line with modern standards
Reset reduces inconsistencies by removing browser defaults, this eliminates all
browser defaults for the page.

##Positioning
static: default positioning, based off type of element and that type's properties
given by html and browser.
relative: the space the element takes in static, left, yet you can still move said
element around on the page. arranged as if everything was in normal position yet
element can move around, this can leave space. Relative to itself and those around
it.
absolute: the element is taken out of the flow of the layout and is placed exactly
where you want it, not common because it can conflict responsiveness.
fixed: positions the element relative to the viewport, good for important
information
sticky:

top, bottom, left, or right (without margin or top) are outside of box model
top and margin-top are not the same thing

psuedo-classes are denoted by :
  used to describe an element that cannot be described by adding a class or
  id user interaction, as well as uses aspects of an element to describe it, to
  avoid giving an element a class or id.  
psuedo-elements are denoted by ::

  great to play on codepen.

  
