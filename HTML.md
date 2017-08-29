# HTML Style Guide
A style guide for HTML.

Writing effecient HTML guidelines means
  1. Smaller download size
  2. Quick rendering
  3. Efficient maintenance

## Table of Contents

  1. [Keep a tidy & shallow DOM](#shallow-dom)
  2. [Use semantic elements](#semantic)
  3. [Do not use iframes]
  4. Minimize/remove non visible text
  5. Tables are bad for non-tabular data
  6. Tag & attribute names should be in lowercase
  7. Attribute values in double quotes
  8. All element should be closed, except self-closed tags (hr, br)
  9. For checked/disabled don’t include attribute values
  10. No onclick attribute
  11. No style attribute
  12. [Accessibility](#accessibility)

<a name='shallow-dom'></a>
## 1. Keep a tidy & shallow DOM
  
  Keep the DOM as shallow as possible. Div soup is a common problem, where each element is wrapped in a series of divs that each apply a single class or style. Many wrapping divs can be collapsed, adding their styles to a single wrapping div or even to the base element.

```html
<!-- Bad -->
<div class="foo">
  <div class="bar">
    <h1>Content Header</h1>
    <p>Lorem ipsum.</p>
  </div>
</div>

<!-- Good -->
<div class="foo bar">
  <h1>Content Header</h1>
  <p>Lorem ipsum.</p>
</div>
```

**[⬆ back to top](#table-of-contents)**

<a name='accessibility'></a>
## 12. Accessibility

  Accessibility shouldn't be an afterthought. You don't have to be a WCAG expert to improve your
website, you can start immediately by fixing the little things that make a huge difference, such as:

* learning to use the `alt` attribute properly
* making sure your links and buttons are marked as such (no `<div class=button>` atrocities)
* explicitly labelling form controls

```html
<!-- Bad -->
<h1><img alt="Logo" src="logo.png"></h1>

<!-- Good -->
<h1><img alt="My Company, Inc." src="logo.png"></h1>
```

**[⬆ back to top](#table-of-contents)**
