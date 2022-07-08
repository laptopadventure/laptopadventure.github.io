# Daily Reading 2 Notes

[Back to the table of contents](../../README.md)

## HTML Chapter 2: "Text"

This chapter goes over text tags, and `<p>`. Surprised we didn't go over that yet! Anyways, `<b>` for bold, `<i>` for italic. super and subscript are `<sup>` and `<sub>`, which makes sense. Then we have breaks `hr` and `br` (forgive me for abandoning the tag containers), and I've made a lot of use out of before. Specifically br, very often used tag since having manual control on when a specific line ends is powerful. Of course at some time in the future proper use of `div` can also bring good results for keeping text contained, but nonetheless great tool to have. `strong` and `em`, which are important and emphasised respectively. They just assume bold and italic, but maybe it's an interesting option to consider changing them in CSS instead of changing the bold tag, which should be kept strictly bold. Blockquotes are indented paragraphs for extended quotes, which work wonderful with some styling... and `q` is for quotes and is kinda useless from what my experience and the lack of global use. `abbr` is an inline tag for showing a... tooltip, I think. The book doesn't specify but that's what it looks like. Seems cool! `cite` is for citing sources, and `dfn` is the first instance on a page of a new term. Kind of like how wiki pages only link to other pages on the first mention. `address` works like `a` but is for the specifically the author of the page. Maybe useful in an about page, but I dunno. `ins` is inserted text which comes out looking like an underline (neat), and `del` is deleted text that comes as a strikethrough. I love using strikethrough but only in a casual setting... still, good tag. `s` is strikethrough, by the way! So don't edit strikethrough on the CSS, edit `del`... seems like a niche case. And that's the chapter! Mostly just learning tags.

## HTML Chapter 10: "Introducing CSS"

Trying something out to see if it makes for better notes, I'm going to take the three topics the chapter says and fill out those sections.

### What CSS Does

CSS is Cascading Style Sheets, and it's how you style the tags in your HTML website! They go hand in hand, and no HTML site worth its salt is without CSS. We learned in our first lecture that you can use `style` tag in the head to write CSS in HTML but that is pure sin really so CSS will be in its own page with its own file ending (.css)

There are several advantages to CSS in a different page instead of the style tag:

* All of your pages can link to said CSS file, preventing copy pasted code. Change the style sheet, change every page.
* One file for CSS means only one stylesheet the user visiting your website has to load, which means for quicker loading.
* CSS files can have better time catching problems with CSS in said file

### How CSS Works

In CSS you define selectors (modify all `p`), for example. After picking which tags you want to style, you define properties in the selector that you wish to give values. For example:

```css
p {
  color: "blue";
}
```

In this, we're selecting all paragraphs, and changing the color of them to blue. Quite simple, and quite powerful. You can select as many tags in your selector as you want too.
There's a ton of special ways to select tags specifically, all of them very neat, but I'll only talk about THE MOST IMPORTANT ONE! Class selectors! My beloved spans that apply a class to everything inside of it can now have their classes equal css styling, and this is my bread and butter for css. Classes are everywhere and you'll see them if you open a dev
console on any website.

And here's another cool part! Cascading Style Sheets... cascade! What that means is that the more specific a style is, the more power its properties have over other selectors. For example, `*` selects everything on the page, and a selector for `p` would override that. And then, if that `p` had a class and that class was a selector, that would override the `p` selector. In practice it works wonders.

## JS Chapter 2: "Basic Javascript Instructions"

I've worked with backend quite a bit so I'm going to try and be a little quick about this part. Variables are made up of the keyword and the var name, and you can set the var name to equal a value. Then checking that variable name later, it will stand in for the value you assigned it. Values come in data types of which there are quite a few, examples being numbers, strings of text, and boolean values (true or false). One interesting thing in the chapter is that it mentions the javascript way to get an element in your HTML and modify it, which is pretty sweet. String definition works a lot like numbers but you have to be careful about using double quotes or singlequotes only, and you can escape characters with `\`. There's some other stuff you'll want to escape but i'm sure that comes later, just know that's an all around tool. Finally, you can set variables whenever. Kinda. There are things like `const` that are variables that are read-only, and there are some situations where vars can't be editted, but for now just assume you can define a variable as something and set it whenever.

### Speed Round: Arrays

We go through some arrays, which are lists that hold data inside themselves, and the techniques for accessing them. They innately have a `length` property for getting the length of the list (how many items are in it).

### Speed Round: Expressions and Operators

Expressions are a set of values and logic that return one value. For example, `var mathResult = 1 + 1` is an expression. The expression itself sets `mathResult` as 2, because 1 + 1 resolves and turns into 2, which leaves us with `var mathResult = 2`. Neat!

Operators are math signs from math class, and more. Examples of operators are +, =, !. They evaluate expressions just like math. Parentheses are a notable case as expressions inside of them resolve first. Again, just like math, it's PEMDAS. Parentheses > Exponents > Multiplication > Division > Addition > Subtraction.

### String Operations

Strings work with +, they concatenate the strings together. For example, `var stringResult = "hello " + "world"` will set `stringResult` as "hello world". Keep in mind that I needed to specify one of the two strings to have the space to concatenate them with a space, everything is explicit here.

### Rules for Naming Variables

Gave this its own section because it's important. The book's rules for naming variables are...

* A name must start with a dollar sign, an underscore, or most likely, a letter. You can't start one with numbers or a boolean or any of that nonsense.
* Then after the first character you can put anything except for `.` and `-`, which are for other things.
* You cannot use keywords. You can't write a var with the name "var", nor would you want to as that's an incredibly nondescriptive var.
* Cases are different characters, "Score" and "score" are different vars. Don't use this to name two different vars the same thing!
* Use descriptive var names. `firstName` and `lastName` make for great descriptors, `N` does not. Single letter var names should be sparse!
* Use camelCase! That means the first character is lowercase, but the next word in the variable is capitalized. Examples in the last bullet point of that. This is more a rule for javascript as a language, You should listen to contributing guidelines of whereever you're working but I'd be very surprised if any javascript environment allowed anything but camel case for naming.

## JS Chapter 4:

In this chapter we'll talk about conditions, loops, and heck, more operators.

### Conditions

So we have ways to get data, now we're introducing ways to check their state. What is this variable I got from a function? What is the state of this instance? We find out with `if ()` checks. They evaluate an expression inside of them, and if the expression is true, then a code block is executed after it. Otherwise, it passes it. You can also define `else` afterwards to run a different code block if the statement doesn't pass. The code blocks are indented to show they only go off in certain cases.

### Operators

We now have some operators which return booleans, because we're not expecting an answer from the evaluation but rather the truthfulness. `1 + 1` returns 2, but `1 == 1` returns `true`, that boolean data type we learned. There are many conditional operators but I won't list them out here. Just know that generally, you want one operand, then a condition operator, then another operand. Remember that parentheses make a conditional execute before the other.

Oh, and we have logical operators, ones that return true or false based on the truthfulness of two conditional operators. `(1 + 1 == 2) && (1 + 2 == 2)` will return false because both statements aren't true.

### Speed Round: Switch Statements

NOTE: This wasn't actually supposed to be read and noted yet, SORRY!


Switch statements are like `if ()` checks but you have any number of code blocks for any number of results from an expression's return.

```js
switch(1 + 1) {
  case 2:
    "code here for whatever happens if 1 + 1 evaluates to 2"
  case NaN:
    "oh god the universe is breaking and 1 + 1 just evaluated to not a number!"
}
```
