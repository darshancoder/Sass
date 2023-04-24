# Sass
Sass Learning Here Super Power of CSS


## 1 Varibles in Sass
- We Define Varibles By using $ sign
- Example Here
`<code> // Sass Varibles Here Goes
$primary-color:#272727;
$accent-color:#ff652f;
$text-color:#fff; </code>`

## 2 Map of Sass
- example
`$font-weights:(
    "regular":400,
    "medium":500,
    "bold":700
)
.main{
    font-weight: map-get($map:$font-weights , $key:bold );// Short Hand  font-weight: map-get($font-weights , bold );

}
`


## 3 Nesting of Sass
- 2 Types Nested Here
1. `.main {
    width: 80%;
    margin: 0 auto;

    // p{
    //     font-weight: map-get($map:$font-weights , $key:bold );
}`

2. `.main {
    width: 80%;
    margin: 0 auto;

    #{&}__paragraph{
        font-weight: map-get($font-weights , bold );
    }
    &:hover{
        color: pink;
    }
}`


## 4 Sperating Files in Sass or Importing Files 
1. Step One 
- Creating file by using _(underscore) ex:_example.scss

2. Step Two 
- Add Your code in that sass File in example.scss 

3. Step Thrid
- import Your File to Main.scss
- `@import './'example`


## 5. Function in Sass
1. Write Function 
- `@function [weight]($weight-name){
    @return map-get($font-weights, $weight-name)
}`

2. Call the Functions
- `font-weight: [weight](medium)`


## 6. Mixin in Sass
### Example One 
1. First We have to write Mixin in TOp the Code 
- If we need to pass Argument in mixin we canot its not mandotray
`@mixin flexCenter($direction) {
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: $direction;
}`

2. We Have to Use mixin By property is [@include]
- `@include flexCenter(row); => With Argument`
- `@include flexCenter(row); => without argument `


### Example Two  [`Bg Change Theme`]
1. Create Mixin
- `@mixin theme($light-theme:true){
    @if $light-theme{
        background:lighten($primary-color, 100%) ;
        color: darken($color: $text-color, $amount: 100%);
    }
}
`

2. Use Mixin By [@include]
- `.light {
    @include theme(true)
    // @include theme($light-theme:true)
}`

### Exmaple Three [`Media Query`]
1. create 
- $mobile is decalre Variable
- `@mixin mobile {
    @media (max-width:$mobile){
        @content;

    }
};`

2. Use it Include 
- `Scss @include mobile{
    flex-direction: column;
    background-color: $accent-color;
  }`

## 7. Extends 
1. Create Extends
 - `@extend .main_paragraph1;`
 - Here We are using Above Paragrah_1

## 8. Math Operations
1. 
## 9. 
## 10. 
## 11. 
## 12. 
