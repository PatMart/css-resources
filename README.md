# css-resources

Because, sometimes you have to.

## Preprocessors
CSS preprocessors offer alternative syntax but compile to basic CSS. Things like selector nesting, loops, mixins, and interpolation are just some of the many features they offer. In terms of basic features they're all at pretty much the same level (although, I haven't done an in-depth feature comparison). Looking at just the GitHub repos, Less has 10k followers while Sass has just 4k. However, Sass boasts 5600 commits and nearly 150 tagged releases. Less has about 1800 and 30 respectively. Real usage statistics are hard to come by, but in my experience Sass the most popular, followed by Less. Stylus is only a minor competitor (although it does have nearly 4500 stars and 3400 commits).

### [Sass](http://sass-lang.com/)
It has two syntax variants: `.scss` which looks very much like CSS (i.e. it has braces and semicolons everywhere), and `.sass` which does away with extraneous punctuation. It seems like `.scss` is more popular, for some bizarre reason. Sass is written in Ruby. The Compass gem provides a huge set of Sass mixins for dealing with vendor prefixes, positioning, etc.

### [Less](http://lesscss.org/)
Less is the main competitor to Sass. It's written in JavaScript. The [Bootstrap](https://github.com/twbs/bootstrap) framework is written in Less (although it does now have an official [Sass port](https://github.com/twbs/bootstrap-sass)). The `.less` syntax is pretty similar to `.scss`.

### [Stylus](http://learnboost.github.io/stylus/)
The `.styl` syntax is about as minimal as it gets. Forget semicolons and braces; you can even drop the _colons_ too. Further, Stylus is less picky about syntax &mdash; you're free to keep using punctuation if you want. Stylus is written in JavaScript.

### Which One?
Shoot, I dunno. Maybe these will help:
- [How to Choose the Right CSS Preprocessor](http://blog.teamtreehouse.com/how-to-choose-the-right-css-preprocessor)
- [Sass vs. Less](http://css-tricks.com/sass-vs-less/)
- [Less vs. Sass](http://flippinawesome.org/2014/01/20/less-vs-sass-its-time-to-switch-to-sass/)

## Frameworks
Frameworks provide a foundation upon which you can build your project's visual style. They also provide features like built-in responsive grids, which are tricky to implement from scratch. Most frameworks are built on either Sass or Less, which makes customizing them pretty painless, since you can jump into the source files and change variables easily, then recompile.

### Bootstrap
[Bootstrap](http://getbootstrap.com/) is the [most starred](https://github.com/search?q=stars%3a%3E1&s=stars&type=Repositories) repo on GitHub by a massive margin. It gives you a quick way to start building a nice-looking page with very little overhead (aside from looking up the proper class names in the docs). However, in a serious project that will involve lots of custom CSS, Bootstrap can be a nightmare. Overriding styles is a tedious exercise in [selector specificity](http://www.smashingmagazine.com/2007/07/27/css-specificity-things-you-should-know/). Further, the popularity of Bootstrap means that sites that use it heavily don't really stand out. They just look like everything else. Bootstrap covers just about every element you'd conceivably use, and as such, is quite large &mdash; around 100KB minified. 

### Others
[Foundation](http://foundation.zurb.com/) is the most prominent Bootstrap competitor. Other CSS frameworks include [Pure](https://github.com/yui/pure/), [Gumby](https://github.com/GumbyFramework/Gumby), and [Blueprint](https://github.com/joshuaclayton/blueprint-css).

### None
I've found that the best way to keep CSS light an manageable is to _not_ use a framework. You'll probably want to start with a responsive grid system and build out from there.

## OOCSS
Object-Oriented CSS applies some of the principles of object-oriented programming to CSS design and structure. The goal is to write modular CSS that scales well.
- [Introduction to Object Oriented CSS](http://www.smashingmagazine.com/2011/12/12/an-introduction-to-object-oriented-css-oocss/)
- [oocss.org](http://oocss.org/)
- [stubbornella/oocss](https://github.com/stubbornella/oocss)
- [OOCSS + Sass](http://ianstormtaylor.com/oocss-plus-sass-is-the-best-way-to-css/)

## Responsive
I feel like whenever someone tries to define exactly what constitutes "Responsive Web Design" they get torn to pieces. So, uh, basically, your site or web app should look good on all devices. In the context of CSS this means, basically, **media queries**. Read the [docs](http://getbootstrap.com/css/#grid) for your responsive grid system, and use them. If you want to go the extra mile, implement some [responsive typography](http://trentwalton.com/2012/06/19/fluid-type/). 