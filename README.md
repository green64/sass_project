# Sass is Where's It's At
[Sass project](https://green64.github.io/sass_project/)

This project has really excited me about Sass and made me want to dig in deeper to learn about everything I can do with it. I used Prepros for my preprocessing tool and it worked great. Easy to get up and running with, very straightforward to use &mdash; I'll definitely use it going forward. 

## Control colors and more with variables

Using variables for hex colors? Hello time savings!

```$deepBlue: #f8f9fb;```

Even more awesome is Sass's built-in lighten feature that lets you control what shade of your variable you use. Perfect for rollovers and no doubt dozens of other uses.

```&:hover{
      background:lighten($deepBlue, 6)
      }
```

## Make Sass do the math

Hands down this is probably the coolest Sass feature I've used so far:

```li{
    float: left;
    box-sizing: border-box;
    text-align: center;
    width: (100% / 3);
  }
```

See that last line? Sass is basically diving the available space among my li tags. This is what it looks like on the page:

![Evenly spaced lis](https://www.samanthamccallfp18.com/assets/images/evenly_spaced_lis.png "li elements")

Beautifully spaced with no math on my part. Pure genius.

## Mixins take control to new levels

Say your site has multiple banners. Just give them the same class (.banner-content in this case) style them with a mixin, and wherever you want to replicate that style, voila:

```@mixin banner{
  width: 100%;
  position: relative;
  color: white;
  .banner-content{
    position: absolute;
    top: 50px;
    width: 100%;
  }
```

## Modularize and import just like React

But Samantha, doesn't your Sass file get awfully messy with all those variables and mixins? No! Because just like React, you can create separate files that all point to your primary Sass file:

```@import "reset";
@import "variables";
@import "mixins";
```

Since these are imported into the primary Sass file, you have to remember to tell Prepros not to automatically process them when you make updates:
![Prepros screen](https://www.samanthamccallfp18.com/assets/images/prepros_imports.png "Prepros screen")

## Conclusion

I thought Sass was only for big projects. But now I know it's about convenience, reuse and making things like dividing space &mdash; evenly spacing nav items for example &mdash; easy-peasy.

:neckbeard:
