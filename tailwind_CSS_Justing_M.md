# Tailwind CSS by Justin M
- [[index]]
  

# CSS Syntax

* slector -> is going to be styled
* declaration block -> 

<selector> {
    <property>: <value;>
}

li {
    color: red
}

## Nominal vs Structural
 * Nominal - by name (ex. .custom_button, li, #shopping_list)
 * Stuctural - How the element relates to one another and/or to the pages (ex. list, label)
   * /* Lobotomized Owl */

## Cascade
* DOM cereates a hierarchy
  * Node - every element is a Node
    * Nodes can contain child Nodes
    * Nodes at the same level are sibling Nodes
  * Rules for element inheretance

## Specificity
* Combining propeties can cause conflicts
  * cascade -
* Specificity score (See mozila article on specificity)
  * format is id - class - type

## Organization
* Pages are combined
* CSS is loaded for entire project

### Challenges to Organization Schemas
* Requires proper understding


## CSS Utility Libraries
* Make have use of re-usable classes
* classes are not tieed to any part of projectvery precise effect (often on property/value pair)
* foucus of CSS tends to be on applying class

## Versus UI Libraries
* Bootsrap Bulma
  * Provide pre-built component
    * Pros
      * Require limited knowledge
      * Fast prototyping
    * Cons
      * Hard to modify 

## Tailwind
* Resources
  * official docs
  * screencasts
  * Refactoring UI
  * Third-party
    * PETAL

### Tailwind classes
* Strucrure: 
  * <property name>-<value> -> bg-red-400
  * <value> -> grid
  * <property>-<qualification>-<value> -> boarder-l-green-400
* prefixes
  * <prefix>:<class> -> hover:bg-red-400

## Tailwind Compiler
* Runs alongside project
* Reads a config file(default: tailwind.config.js)
  * Is made aware of parts of the project where Tailwind files are located
  * Theme and plugin configuration
* Generates a style sheet during development for instant feedback (ex live-reload)
* 
  

### BEM (Block, Element, Modifier) - Class naming structure


Question:
* Link to mozila article(s) on specificity
* Language server: Do you mean for the CSS language?

## Tailwind Survey
- Responsive
  - modifiers
    - 5 by default: sm, md, lg, xl
- Pseudo Elements/classes - refer to only portions of an element or add the page in addtion to what HTML would have provided
  - Provide things like different strategies
    - visited
    - hover
    - before
  - Arbitrary Value Syntax
    - `class="before:content-[attr(before)])`
  - Theming - Makes it possible to modify tailwindcss 
    - Relies on tailwind.config.js and is applied by Compiler
      - configuration file (ex font-stack, colors, sizing scale)
  - @apply - Makes tailwind apply the themes
- Background Images -
  - Gradients
    - bg-gradient-to-<direction>
    - from-<colour>
    - to-<colour>
    - via-<colour> : intermedient color
    - color stops: ex from-10%, via-40%
  - supports different state (ex hover)
  - Limitations 
    - no gradient Typesmore than 1 mid-colour 
    - more than 1 mid-coulor
  - backgroundImage Class 
    - set in tailwind.config.js themes
    - can use arbitrary value syntax
- Dark Mode - media query
  - applied similarly to psuedo-classes
- Animations
  - a few prebuilt 
  - tailwind-config.js  
    - keyframes property
- Hero Icons - Maintained by Tailwind

## Tailwind w/ Phoenix
- Default with 1.7
- Tailwind hex package - easiest path to apply to older projects
- Main Setup
  - inculde congig to start compiler-watcher 
  - include task
- Phoenix Component Templates
  - Phoenix TEmplates can include properties as 
    - stirng or
    - inetpolated inside {}
    - Just add classes
  - with helper functions
- CSS Property Management
  - Common problem w/ CSS
  - Effectively each class-name represents a line that would otherwise be in css file
  - rout and solution of problem:
    - ordering classes
    - class can be broken onto multiple lines
    - use helper functions - define helpers in .ex file
- Common Problems
  - Interpolation
    - computing a class name ex: `"grid-col-#{@cols}
    - solutions
      - use a helper functions - gets tedious fast
      - tell compiler to always generate the classes
      - inline style `style="
    - Duplication
      - classes modifying the same property ex 
      - ```
        <div class=>
      - solution 
        - Dont provide default classes to parent
        - Use merge function provided by Tailwind

## Resources
- Front End Masters CSS path
- Keven Powel youtube channel
