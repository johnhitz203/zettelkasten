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