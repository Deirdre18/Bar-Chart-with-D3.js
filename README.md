## This is an D3 lesson (from Code Institute Full-Stack Diploma course). Transcription from lessons, included in comments sections in the code. 

# Creating bar chart with D3.js

1. What is it?

D3 Bar Chart

2. What does it do?

Programmaticaly binds data to an SVG to create a graphical display of the data using bars of different heights.

3. How do you use it?

Bind the data to an SVG element called a "rect". Do this for each datum in the data set. Set the attributes for the rects and target a div id to render the resulting bars.


LESSON:
At this point we have been introduced to SVG's - the fundamentals of scalable
vector graphics. We've been introduced to the basics of D3 which manipulates and
works on scalable vector graphics. But it does it programmatically using
javascript. Now let's look at creating a bar chart similar to the one we created
a couple of Units back but this time creating it programmatically using D3. So
we have a data set here of discrete integer values and we are setting our
height with a bar padding variables for use later on. This pattern is quite
common - we use our D3 object to create an SVG object. We're using Select and
the Select ties our viewport to a div with an ID called draw-here.
once we've that done we then append an SVG as a child of that div it's part of
the document object model and the height and the width of that viewport is
determined by the H and W variables which we define on lines 17 and 18 now
we're setting up our bar chart
you
and on line 34 we define what the rectangle will look like so we append a
rectangle going to give it its X&Y coordinates its height and its width so
let's do let's set the x coordinate and again this would be a function and the
function U takes in two parameters our uses two parameters d and i is the
data which is the actual value in a in the data set array and I is the index of
that data and the x value is going to be the width divided by the data set length
i remember the length property is available on every array in JavaScript
okay let's set the Y value for each bar and the height - d
now let's set the rectangle height and it'll be d that'll be the actual value
of the data at that point in the array
let's set the width and the width will be W divided by the data set length
minus the barpadding let's check that there
you
and there you have it there's our bar chart you can see the heights you can
see the padding and again the default color is black because unless you
specify otherwise both text and textual elements will be rendered in black by
default in the browser so let's refactor this a little bit just do a little bit
of cleaning so let's set the column width so we're just being a little bit
more efficient here with our variables are very very you suggesting the wrong
place let's move it down because otherwise we're trying to access a
variable called data set that has yet to be defined remember by default
javascript interprets variables in the order they appear so that's replace our
earlier calculation with call width we can actually clean this up even more
it's called the bar with so we can remove those and clean up our code
doesn't necessarily improve our they the execution speed but it makes it a little
bit more elegant and more readable okay and that works so what we'd like to do
now is we would like to make our data visualization our bar chart that little
bit more informative that a little bit more visually visually richer and in
order to do that let's display the actual values the integer values for
each bar represent them on the bar itself in other words they they the data
entries are the datums inside in the data set let's display those on the bar
each bar element itself to provide a richer feedback to the viewer so in this
case we use a text object again we bind the text to the data set that's where we
get our values from so for each entry in the data set there will be a text object
created now online 57 you can see they there's a an attribute it's an SVG
attribute called text anchor and we're setting it to middle it's a bit like m
in a normal text editor such as word or so on you have left align middle and
right align so we're we're Center aligning our text on the bar itself and
we're setting some additional text properties such as the font family sound
serve and default sound service and giving it a font size of 11 pixels and
we're going to fill the text element with the color white you can use M
hex values as well we're just using the
the web palette representation that limited web palette representation just
for simplicity
now notice are the Y value were using the height minus D plus 14 so it'll be
14 pixels down from the top of the bar itself it's positioning and we're
specifying the x-coordinate of our entry in the middle of each bar chart so you
can see it there more informative richer we're moving along nicely we're now
using d3 to programmatically bind data to SVG's and represent them in a visual
format
