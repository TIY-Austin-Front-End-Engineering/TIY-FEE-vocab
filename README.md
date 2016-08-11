# TIY-summer-review

## HTML
* Doctype ( interview question: what does doctype declaration do )
* Meta tags
* Anatomy of an HTML tag

      ```html
      <tagname attributeName="value"></closingtag>
      <selfClosingTag />
      <!-- comment Write a bunch of stuff here-->
      ```
* Linking to external stylesheets
* Linking to external javascript files
* Forms and form accessibility - `for` attribute should match `id`. all inputs should have a `name` attribute.
* Data attribute - Use to store extra data about a particular element. Access that data with Javascript.

## CSS
* Anatomy of a CSS ruleset

      ```css
      selector {
        property: value
      }
      ```
* Specificity ( interview question: order elements from most to least specific )
* Block vs inline elements ( interview question: describe the difference, give examples )
* Box model - content, padding, border, margin
* Float vs {display: inline-block} vs flexbox
* Collapsing margins
* Units of measurement - px, percent, em, rem, vh, vw
* Pseudo elements and pseudo classes
* Positioning - static, relative, absolute, fixed, sticky
* CSS resets
* Media queries

      ```css
      @media media-type and (parameters) {
        selector {
          property: value;
        }
      }
      ```
* Transitions - There are four transition properties:
    * `transition-property` - the property that will transition, e.g. `background`
    * `transition-duration` - the duration of the transition in seconds, e.g. `2s`
    * `transition-timing-function` - defines a function that describes how the transition will proceed over its duration, for example starting slowly and speeding up toward the end of the transition. Values include `ease`, `linear`, `ease-in`, `ease-out`, `ease-in-out`, `step-start`, and `step-end`
    * `transition-delay` - the amount of time, in seconds, that should pass before the animation begins
* Animations - use keyframes and subproperties to animate elements

## Sass
* Partials - separate Sass files into components, import partials into main sass file using `@import 'partialName'`. Note: when naming partials, use an underscore, e.g. `_variables.scss` as the first character, but import without the underscore.
* Nesting - child elements that inherit properties from a parent can be nested inside the parent's ruleset. You can also nest pseudo selectors.

      ```sass
      .dropdown-menu {
        a {
          text-decoration: none;
            &:hover {
              text-decoration: underline;
            }
          }
        }
      ```
* Variables - Used to store repeated values. Denote with $, e.g. `$main-text-color: #8a8a8a`
* Mixins - Used to store repeated rule sets

```sass
      @mixin imageBox {
        height: 200px;
        width: 200px;
        border: 10px solid white;
        box-shadow: 0px 0px 5px 0px rgba(0,0,0,0.25);
      } 
```
* Bourbon - Sass mixin library
* Neat - Sass grid system built with Bourbon mixins

## Web Design Practices
* Pixel perfect
* Responsive vs adaptive design

## Command Line
* Beginner command line syntax - `cd`, `..`, `pwd`, `ls`, `mkdir`, `touch`, `cp`, `rm`, `clear`, `mv`, `clear`, `tree`, flags (`-rf`, `-a`, `-s`, etc)

## Git
* Beginner Git syntax - `init`, `remote`, `status`, `add`, `commit` (`-m`), `push`
* Branching - Create new branches for each feature of your project. Branch commands: 
      * Create new branch and check that branch out: `git checkout -b <branch name>`
      * Check out exising branch: `git checkout <branch name>`
      * List all branches: `git branch`
      * Rename the current branch: `git branch -m <new branch name>`
      * Push branch to github: `git push origin <branch name>`
* Pull requests and merging in GitHub
* After merging branches in your remote, pull changes to local repo: `git pull origin master` or `git pull origin` to pull changes while on a feature branch
* Cloning - save a copy of a repository to your computer: `git clone <remote repo path> <local folder>`

## JavaScript
* Type coercion
* Accessing the DOM with vanilla javascript: `document.querySelector()`, `document.querySelectorAll()`, `document.getElementByID()`, `document.getElementByClassName()`
* Vanilla javascript event listeners: `element.addEventListener('nameOfEvent', functionToRun)`

## Useful Tools
* [caniuse.com](http://caniuse.com)
* [Pixel perfect chrome extension](https://chrome.google.com/webstore/detail/perfectpixel-by-welldonec/dkaagdgjmgdmbnecmcefdhjekcoceebi?hl=en)
* [Responsive Web Design Checklist](http://rwdchecklist.com/)
* [List of DOM events](https://developer.mozilla.org/en-US/docs/Web/Events)
