# RSCSS CHEAT SHEET

## Summary 
```css
/* Naming Components */
.like-button
.search-form
.article-card
.alert-box
.alert-card
.alert-block

.link-button
.link-span


/* Naming Elements (uses '>', only one word) */
.search-form {
  > .field { /* ... */ }
  > .firstname { /* ... */ } 
  > .lastname { /* ... */ }
}


/* Variants */
.search-form
.search-form.-prefixed
.search-form.-compact

```


## Avoid positioning properties

Components should be made in a way that they're reusable in different contexts. Avoid putting these properties in components:

Positioning (**position, top, left, right, bottom**)
Floats (**float, clear**)
Margins (**margin**)
Dimensions (**width, height**) *

\* *Exception to these would be elements that have fixed width/heights, such as avatars and logos.*

If you need to define these, try to define them in whatever context they will be in. In this example below, notice that the widths and floats are applied on the list component, not the component itself.

```css
.article-list {
  > .article-card {
    width: 33.3%;
    float: left;
  }
}

```

## Helpers
Use them very sparingly.

```css
._unmargin { margin: 0 !important; }
._center { text-align: center !important; }
._pull-left { float: left !important; }
._pull-right { float: right !important; }
```

## One Component Per File

```css
/* css/components/search-form.scss */
.search-form {
  > .button { /* ... */ }
  > .field { /* ... */ }
  > .label { /* ... */ }

  // variants
  &.-small { /* ... */ }
  &.-wide { /* ... */ }
}
```

http://rscss.io/
