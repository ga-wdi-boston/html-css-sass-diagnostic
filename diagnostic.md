# Sass Diagnostic

Place your responses inside the fenced code-blocks where indicated by comments.

## Sass Variables

We have a color literal, `#6495ed`, that we want to store in the variable named
"cornflower". Write the Sass code necessary to assign the color literal to the
desired name.

```scss
$cornflower: '#6595ed';
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
  $base-font-size: font-size * 1.3;
}
```

Now, suppose you have a `$base-margin` defined as below. Write a style rule to
**halve** the base margin, but only for list item elements.

```scss
$base-margin: 1.5em;
```
// I am not sure if you can make the variable part of the value like this, but // it is the only way this makes sense to me... we are setting the more general // base margin to be the value after halving the given $base-margin.


```scss
li{
  base-margin: $base-margin/2;
}
```

## Functions

Suppose you have a function available, `tint`, which takes two arguments. The
first argument is a base color, and the second argument is a percentage. `tint`
will take the base color and lighten it by the percentage indicated by mixing it
with white. Write the code to tint `$cornflower` by 20%.

//I believe we are just calling the function with the arguments....

```scss
tint($cornflower, 20%);
```

## Mixins

Suppose you want to define a mixin named `row` stored in `./row.scss`. Write the
code to import the mixin definition in the current module.

//we are apparently already in the current module, so if we only want to import //the definition of a mixin located where we are already inside of, then it //should be straight forward. I am not sure if this is a trick question though, //because It doesn't make sense to me that you would import a mixin when you are //already in the file you are supposed to be importing to. That is not my //understanding of what @import is supposed to do, but it seems to be what the //question is asking.

```scss
@import 'row';
```

Now that the mixin is imported, let's use it. This mixin doesn't take any
arguments. Write the code to include the mixin inside all elements with a
class of `content`.

//If I answered the previous question correctly, then I just need to put that //mixin inside of a content class, I think. 

```scss
.content{
  @import 'row';
}
```
