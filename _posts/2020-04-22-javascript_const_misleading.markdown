---
layout: post
title:      "Javascript const misleading"
date:       2020-04-22 19:32:36 +0000
permalink:  javascript_const_misleading
---


just a quick post on the javascript const variable. how something like the name const in javascript is misleading. I worked on practicing variables today and I came across a problem when I ran my local test. which was that the word const doesn't mean const when it comes to javascript that is. a perfect example  

``` 
const PI = .0023333  ;
// correct
const pie = 'numbers';
// also correct
const array = '{}';

const PI = .33333
// incorrect
PI = .2222
// inscorrect
```

my understanding is that the word const and the idea behind it allows a variable not to change or reassign. you would use the const variable if you wanted your value to stay the same.

thanks for reading 😀
