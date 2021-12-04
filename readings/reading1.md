# Daily Reading 1 Notes

[Back to the table of contents](../README.md)

## Chapter 1: "Structure"

> This chapter begins by explaining the conceptual side of the HTML page, with comparisons to the user experience of a webpage as an introductory
segway into explaining how the structure of those websites looks codeside. One concept explained is hierarchy of information. Websites are huge
pages of information and the design of the webpage is based around the idea of deciding which information on the panel is more important and
should be shown sooner than others. The chapter then gives a diagram of the HTML structure, where elements hold elements and information (body
holds body elements, p holds strings of text, etc). Finally, it introduces attributes as properties of specific elements on the page.

## Chapter 8: "Extra Markup"

> We start with a history of past versions of HTML, which details some interesting notes like tags needing to self close. I was a bit sad
to see that gone in HTML5, since requiring closing or self closing tags is something i'm more used to. Anyways, despite HTML5 being in active
development, it and its features can still be used. The chapter quickly explains how to indicate to the html which version its using (in case you
wanted a legacy version of HTML). Explanation of comments, which I'm not a huge fan of either in all honesty. Lack of an end of line comment and a
very long syntax for the comment discourages use when comments should be plentiful. We head into the ids (meh), classes (cool), and spans (super
cool). These are used to apply css to specific elements. Divs are spans but not inline, of course, making them good tools for grouping elements.
Meta entries are information that isn't shown to the vistors of your site, but rather robots that visit your site, one example being search engines.

## Chapter 17: "HTML5 Layout"

> This chapter focuses on the specific new changes brought in with HTML5. One of the big things here is that HTML5 turns what would be class
attributed divs into their own generic elements, one example a div with a header class attribute at the top of the page being turned into simply a
unique element, `<header>`. This helps accomplish what people generally try to add to a website (headers are common and are on a ton of sites,
right?) along with some extra other elements such as "asides", "nav", "footer", and more. The names are pretty self explanatory except for asides,
which is an element for a side section. Speaking of which, sections! They're (usually) combined with a header to group related content together. One
of the most powerful tools HTML5 gives is the ability to make entire groups a link, which is pretty glorious in action. Older versions of html do not
play well with these new tools so google provides free javascript to replicate their functionality on older machines. Neat!

## Chapter 18: "Process and Design"

> Okay, so this is isn't really about code as much as it's about design. What is your site trying to do? Okay, and who are its target users? There's
a big section about considerations with your customer. Since what you offer is information and services, if you successfully deliver that information
and or that service, you're ensuring people can return to your site to get what they need. Which brings us back to Chapter 1 for a callback to the
idea that the goal is to prioritize the most important information to the visitors first and foremost with your elements. Developers map out their
website by providing site maps (which webpage on your site leads where? Your landing page has access to other sites that show certain things for
users to seek out? That's the idea.) and also wireframes, for specific pages. These entail showing the barebones of how much each element group
should be taking up and what they display... without what they display added yet. Group your thoughts, prioritize important information, and an easy
way to get around ensures a happy visitor. Use all the tricks at your disposal. Bolding, coloring, grouping, all of these are techniques to organize
and present your information.

## JS Chapter 1: "The ABC of Programming"

> Now we're on the Javascript side, how fun! We begin much like the HTML book by diving into the concepts of what a script is, what an object is, and
what an instance is. Scripts are instructions that complete a goal, objects are types of data that hold values describing themselves, and instances
are created objects, a bit of memory allocated to holding this object and its values, which then can be permutated. By checking the state, a script
may act differently. One of the most important takeaways is that a computer thinks differently than we do, and nothing is known unless you tell it,
or it finds out with logic. With this in mind, breaking your scripts into chunks of logic is helpful for coding as you want to be able to squash bugs
in your code as they come, instead of moving onto adding new logic with broken code laying dormant to error in the future in possibly more obfuscated
ways.