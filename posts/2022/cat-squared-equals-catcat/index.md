<!--
.. title: cat² = catcat?
.. slug: cat-squared-equals-catcat
.. date: 2022-12-15 21:22:07 UTC-05:00
.. tags: language, math, computation
.. category: linguistics
.. link: 
.. description: 
.. type: text
-->

What if I told you that you can do math with language?
What, you didn't think math was about numbers, did you?
Sure, you *can* do math with numbers, but you can also do math with all sorts of things.

Here, I'll show you.
We're going to use *strings*.
These are just sequences of arbitrary symbols.
Traditionally we the lowercase letters *a, b, c, d*, etc., but you could use anything.
I think it would be fun to use little shapes like ♠♣♥♦, but they're too hard to type, so we'll do it the old fashioned way.

A string consists of zero or more symbols in linear order.
So *a* is a string, as is *ab*, and *abcabcaaaaaa*.
There is only one string of length zero, which is called the "empty string".
It's notated ϵ (Greek lowercase epsilon).

So what can you do with strings?
Well, you can stick them together, one after the other.
The fancy word for this is "concatenatation".

*ab* + *cd* = *abcd*

Adding (concatenating) the empty string to either side of another string just gives you the same string back.

*abc* + ϵ = ϵ + *abc* = *abc*

If you've even done any kind of programming, this should be familiar.
Programmers are used to the idea of making up new kinds of objects and operations.

What are some other things you can do with strings?
Well, you can repeat a string some number of times.
This is notated with a superscript, like raising a number to a power.
For example, *a⁵b⁵* is short for aaaaabbbbb, and *(ab)³* = *ababab*.

You can also substitute a string into another.
The notation I've see for this uses a dotted circle (⊙) for this operation, and the string on the left side needs to have a box (□) showing where to insert the string on the right.

*l□r* ⊙ *c* = *lcr*

Okay, so what exactly is this good for?
Well, just as you can use numbers to model phenomena in physics or economics, you can use strings to model language.
I'm still thinking about to talk about this in a way that keeps things light and fun, so you'll just have to wait for part two.
