# IOCSS (WIP)
A front-end methodology for robust/flexible/scalable HTML/CSS/JavaScript.

## Basics
* **Every** HTML element can be a Component.
* Component may has one or more Element(s).
* Element can also be a Component.
* Modifier/State class name isn't a good idea.
* Each Component should know only itself and its own Element(s)/Sub-Component(s).
* IOCSS allows you to use 2 different syntaxes. One is **BEM-like syntax**, another is **Interface-driven syntax**.

(Web Components might also rescue us from CSS nightmares.)

## Class name (BEM-like syntax)
* The class name of each HTML element should be <code><var>component</var> or <var>component--element</var></code>.
* <code>"<var>component</var>"</code> means just **"A <var>component</var> Component"**. This is similar to BEM's Block.
* <code>"<var>component</var>--<var>element</var>"</code> means **"An <var>element</var> Element OF the <var>component</var> Component"**.  
  In other words, **"The <var>component</var> Component HAS the <var>element</var> Element"**. This is similar to BEM's Element.
* Normally, one Element has only 1 or 2 class(es).  
  One is for the Element of a Component, another is for a Sub-Component that is injected as the Element.
* <code>"<var>component--element</var> <var>another-component</var>"</code> means **"An <var>element</var> Element OF the <var>component</va> Component"** and **"The <var>element</var> Element IS also <var>another-component</var> Component"**.  
  This is for **CSS selector delegation**/**CSS selector chaining**.
* Cerate new class name for a variant of Component/Element, instead of using a class name like BEM's Modifier.
* Adding vendor-prefix to each class name is a good idea.

## Common Component Structure (BEM-like syntax)
```
<div class="component-name">
    <div class="component-name--content">
        <div class="component-name--header">
        </div>
        <div class="component-name--body">
        </div>
        <div class="component-name--footer">
        </div>
    </div>
</div>
```

* You may omit each Element.

## Common Component Structure (Interface-driven syntax with Component Interafce)
```
<div class="component-name i-component">
    <div class="component-name i-component--content">
        <div class="component-name i-component--header">
        </div>
        <div class="component-name i-component--body">
        </div>
        <div class="component-name i-component--footer">
        </div>
    </div>
</div>
```

## Resources
* [Example (BEM-like syntax)](http://codepen.io/whizark/pen/vEzbLr)
* [Component with the Structural Interface](http://codepen.io/whizark/pen/OVNPeP)
