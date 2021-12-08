installed a new Atom plugin that renders HTML previews in realtime.

created documentation folder in website repo.

created css stylesheet.

download instagram press packet and figured out how to make an image hyperlink to my instagram.

figured out (by guessing) that I could create different html pages for parts of my site and use relative linking to get there.

originally had adapted an entire css code for a side navigation bar, but the usage license from the website wasn't clear enough for me to feel comfortable. instead, I'm going to try and recreate it from scratch using mozilla's open source css samples.

mozilla's resources are sick also I am starting to grasp CSS and actually understand why things need to be certain ways. most of my code is entirely me at this point.

experimenting with basic color scheme balancing in my css before going on to add much more.

checked mozilla to learn how to add link hover color change for text.

watched a video and learned how to write a .htaccess file in Apache to hide the .html extension of my pages in the URL bar.

after reading some other people's code (mainly by analyzing professional websites) I realized that I could improve the readability of my code by using indents (not required for HTML to work, unlike python), so I did.

COOL! you can set one dimension for image scaling to 100% and then change the other dimension and it will retain aspect ratio.

so the thing is, I think there's a more efficient way to abstract out common CSS for each of my pages. HOWEVER I'm stubborn + I think it gives me the tiniest bit more flexibility if I keep separated CSS sheets.

Fixed overflow horizontal scrolling issues associated with fixed position CSS elements.

going to try and scale up the navigation bar.

(NOTE TO SELF: having the text boxes exist under the "main body text" organizer greatly helps move them together)

Having an issue where my logo and the scrolling blurb at the very bottom of the page are both rendering incorrectly when I open the page in a browser but are rendering just fine in the IDE preview window.

I realized that the positioning for the blurb and the logo were lacking units, which the editor correctly assumed meant pixels, but apparently my browsers did not. Once I added the px unit it rendered correctly.

Did some work today including drawing up a home glyph in illustrator. The one thing I'm struggling with is regarding the Commissions page; on the main page it's simple because I only have one column of text bubbles, but on the Commissions page I want to have one column on top and two columns on the bottom. And I do have this set up. However, the issue is that I want the text boxes to be drawn according to percentage of screen real estate instead of by a designated pixel amount, just like they are on the Main page. However, when I attempt to draw in the text bubbles on the bottom according to percentage, the left one always overflows into the right once the screen size gets big enough. I've tried using padding and margin strings to create a block to stop the bubbles bleeding together, but it hasn't worked. Maybe the best thing to do would be studying the table/column strings for CSS...
