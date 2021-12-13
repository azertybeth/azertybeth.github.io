Set up ATOM as my IDE by installing an HTML preview renderer plugin. ATOM already has an HTML and CSS linter, so I didn't need to install those manually.

I created a documentation folder in the site repository.

I downloaded the instagram press packet and learned how to use <a> with "href" string to have an image point to a link.

I had a hunch that I could create multiple .html files in the repository and locally point to them in the index to achieve having multiple pages. This ended up working.

Originally, I had adapted an entire CSS example code for a side navigation bar, but the usage license from the website wasn't clear enough for me to feel comfortable grabbing it like that. instead, I'm going to try and recreate it from scratch using mozilla's open source CSS code samples.

So far mozilla's resources are fantastic, and at this point my site is entirely hard-coded with no templates.

Experimenting with basic color scheme balancing in my CSS before going on to add much more.

Using mozilla's CSS resources, I implemented a link hover highlight functionality for the navigation bar.

Using multiple .html files to achieve different pages resulted in having ".html" in the URL bar for every page except for my index. Unfortunately, mozilla didn't have very much on this subject, thus I ended up referencing a YouTube guide by Dani Krossing whose entire channel is geared towards free coding resources. The solution to my problem was writing a ".htaccess" file, written in Apache, that communicates to the server to rewrite the URL text and hide the file extension.

After reading some other people's code (mainly by analyzing professional websites) I realized that I could improve the readability of my code by using indents (not required for HTML to work, unlike python), so I did.

After wasting time specifying widthxheight for images on my site despite wanting them to maintain the same aspect ratio, I realized by accident that if I only specified one dimension the entire image would scale with the same aspect ratio.

Created multiple CSS sheets for each of my pages.

Fixed overflow horizontal scrolling issues associated with fixed position CSS elements.

Navigation bar was increased in size to make better use of space.

Drew up individual page glyphs in Illustrator and implemented them as part of the page links in the navigation bar.

Having an issue where my logo and the scrolling blurb at the very bottom of the page are both rendering incorrectly when I open the page in a browser but are rendering just fine in the IDE preview window. I realized that the positioning for the blurb and the logo were lacking units, which the editor correctly assumed meant pixels, but apparently my browsers did not. Once I added the px unit it rendered correctly.

Did some work today including drawing up a home glyph in illustrator. The one thing I'm struggling with is regarding the Commissions page; on the main page it's simple because I only have one column of text bubbles, but on the Commissions page I want to have one column on top and two columns on the bottom. And I do have this set up. However, the issue is that I want the text boxes to be drawn according to percentage of screen real estate instead of by a designated pixel amount, just like they are on the Main page. However, when I attempt to draw in the text bubbles on the bottom according to percentage, the left one always overflows into the right once the screen size gets big enough. I've tried using padding and margin strings to create a block to stop the bubbles bleeding together, but it hasn't worked. Maybe the best thing to do would be studying the table/column strings for CSS...

After meeting with Rachel, I implemented the following changes based on her feedback: unified pages CSS into a single stylesheet, made navbar list universal across all pages with home button at the top, updated blurb at the bottom of the webpage, renamed Projects to Portfolio. I was initially concerned that having separate stylesheets was the only way to contain instructions for elements that were unique to certain pages, though after speaking to Rachel I realized that if the CSS called on a element that didn't exist on a given page, it simply wouldn't do anything, thus it was both functional and much superior to have a single unified stylesheet.

With the deadline for the project around the corner, I'm considering alternatives to the layout I had planned for the Commissions page. I had initially wanted to grasp a deeper understanding on how to take advantage of CSS box alignment and/or table model, but I may have to settle on an alternative since my confidence in grasping those new concepts in the next two days is low.

I wanted to have a large transparent image on the highest z-index but doing so prevented the ability to click on a link underneath the transparent part of the image. After reading a stackexchange forum I learned that I could just add the string "pointer-events: none;" under the image's portion of my stylesheet and it ended up working how I wanted.

After defaulting to an easier option with the Commissions page, I'm going to finally try and implement a table for my Portfolio page. Mozilla's archives have a simple HTML and CSS table code that is barebones and modifiable so I can fiddle around and understand what each string means without doing it from scratch. Using and modifying the table model, I was able to implement a Portfolio layout that I liked. I was struggling to have a set square dimension for one of the cells while also having a percentage-based scale for the overall width of the table but I realized I could use max width instead of just width to achieve my desired result.

The way column spacing is achieved in CSS table elements is a bit odd–as in the only way I can see to do it is to draw a border which ultimately offsets the spacing around the entire data cell and not just between the data cells that are adjacent. This messed up the padding I had between the top of the table/text box that made it look flush with the other pages. Initially, I had fixed this by setting a designated number of pixels down from the top to render the table. However, while this previewed fine in my IDE, it did not render correctly in web browsers. I needed to find a way to have the table be dynamically offset by the header regardless of how the browser scaled it. So, I landed upon using a negative margin string, which compensated for the border drawn without giving the table a static location that would look strange in different browsers.

Overlaid some art I had previously commissioned from a friend on the right hand side of the website. After checking the render in web browsers, I am very satisfied with how my site looks.
