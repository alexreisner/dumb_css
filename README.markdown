Dumb CSS
========

Nobody should lose time from their life solving CSS selector specificity problems. Nobody should have to read 1000+ line stylesheets and nobody should have to resort to a debugger to figure out why an element looks a certain way. Yet these are all things we've come to accept. Fuck that.

Do this instead:

    .float_left { float: left; }
    .bold { font-weight: bold; }
    .large { font-size: 24px; }

Note how much easier it is to understand those rules than ones like this:

    #navbar ul li span { float: left; font-size: 24px; font-weight: bold; }

And that's a generous example. I'm sure you've seen worse, and you know how annoying it can be to come to a new project and have to figure out why an element looks the way it does. **On large projects, finding the relevant styles can be nearly impossible without a debugger, and that doesn't seem like a property of good code to me.**

Sure, this:

    <li class="float_left bold large">Home</li>

may be longer than this:

    <li>Home</li>

but you know what the element is going to look like without searching through CSS rules, and **you can add new, styled elements without writing any CSS at all!** If your CSS rules aren't reusable they're not much better than inline CSS. You've separated them from your HTML but to what end? Your HTML is shorter but your stylesheets are longer and you spend a large part of your life trying to connect the two. Especially when you join a new project...forget about it.

Use these short, "dumb" CSS rules and I guarantee you will _significantly_ reduce the size of your stylesheets and increase your happiness.

What This Is
------------

This project provides a basic set of highly reusable styles. I've stuck to rules which can be applied to _any_ site. You should add others that apply to your specific project, like:

    .small { font-size: 12px; }
    .large { font-size: 24px; }

Don't be stupid and do things like this:

    h1.large { font-size: 32px; }

or worse:

    .header h1 { font-size: 32px; }

You can't reuse those! And worse, some day you or someone you care about is going to spend time _hunting_ for some rule, possibly among thousands of others, because your HTML doesn't give you a damn clue as to why your `<h1>` looks the way it does.

Alright?

No, This Wasn't My Idea
-----------------------

You may recognize reusable classes as one of the principles of [OOCSS](http://www.stubbornella.org/content/category/general/geek/css/oocss-css-geek-general/). You are correct. I am not claiming to have invented anything here, I'm just yelling at you for not doing it.
