## Sass(SCSS) Documentation

Main Difference between Sass and SCSS is, sass used tab based syntax while scss used curely bracket syntax. Also sass do not have semi-colon to seperate statement while scss have semi-colon to seperate statement. SCSS is quite good to right as we have curly braces as an identifier for groupism.

## Variables
- We use variables to reuse the value throughout the codebase, In same way we can define variables and can be used throughout the stylesheet.
- We have to use `$` to make something a variable.
- For example, $p_color: #000; ==> p { color: $p_color; }

## Nesting
- While using the HTML we have used the herirachy to define elements inside elements, while in the same way we can use the sass and nest the selectors as same visual heriarchy for the HTML.
- This also result in problem of over qualified CSS and may be hard to maintain the actual css.

## Partials
- The idea is to create the small css code chunks that can be reused in different files and which can be modularised, which is easy to handle.
- This Partial you can add it to main file so that we can clean the main css file.
- We can have access to all variabls, mixins etc being added on the partial files.
- You can check example of _partial1.scss added on this directory.

## Mixins
- A mixin is used to create the group of css and let you to use where you want it to be exactly like a function in any other lanaguage.
- You can have variable too pass through mixin and acheive dynamic behaviour too.
- You have to use @include function to use mixin in the file.
- You can checkout the `mixin-example.scss` on this directory.

## Extend/Inheritance
- We can share the set of css properties from one selector to another selector by using the placeholder class, which could only be printed if its extended hence making the output css more cleaner.
- You can check `extend-use.scss` file on this directory for more example.

## Operators
- Doing mathematics in Css is now possible, we can use @use "sass:math" and can simple add, subtract, multiply and divide.


## At Rules

### @Use
- Use to load mixins, functions and variables and are called modules.
- We can also access variables from functions, mixins by using <namespace>.<variable_name>.
- To make the vairables private to it own partials file we can start writing vairable name using _ or -.

### @Forward
- It is similar to @use rule and make mixins, functions, and variables available.
- We can also have abililty to hide some of the variables, members etc when forwaded is being used. For example, @forward "src/list" hide list-reset, $horizontal-list-gap;

### @Import
- 