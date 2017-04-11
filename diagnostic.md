# Sass Diagnostic

Place your responses inside the fenced code-blocks where indicated by comments.

## Sass Variables

We have a color literal, `#6495ed`, that we want to store in the variable named
"cornflower". Write the Sass code necessary to assign the color literal to the
desired name.

```scss
$cornflower: #6495ed;
```

Write the Sass code to access the variable once it has been defined.

```scss
a {
  color: $cornflower;
}
```

## Arithmetic

Suppose you have a variable defined, `$base-font-size`, that sets the font-size
on the body element. Use that variable to increase font-size of `h1`
elements by 30%.

```scss
h1 {
  font-size: $base-font-size 20%;
}
```

Now, suppose you have a `$base-margin` defined as below. Write a style rule to
**halve** the base margin, but only for list item elements.

```scss
$base-margin: 1.5em;
```
li {
  base-margin: $base-margin (halve);
}

// or maybe just base-margin: 0.75em;
// or maybe base-margin: $base-margin 50%;
```scss
// your response here
```

## Functions

Suppose you have a function available, `tint`, which takes two arguments. The
first argument is a base color, and the second argument is a percentage. `tint`
will take the base color and lighten it by the percentage indicated by mixing it
with white. Write the code to tint `$cornflower` by 20%.

```scss
$cornflower: tint( $base-color, 20% );
```

## Mixins

Suppose you want to define a mixin named `row` stored in `./row.scss`. Write the
code to import the mixin definition in the current module.

```scss
@import './row.scss'
```

Now that the mixin is imported, let's use it. This mixin doesn't take any
arguments. Write the code to include the mixin inside all elements with a
class of `content`.

```scss
content {
  @include row
}
```
