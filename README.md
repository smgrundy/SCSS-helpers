# SCSS-helpers
Quick SCSS to create margin / padding helper classes over multiple breakpoints in both px and %

This is a file that I've used quite heavily in recent projects. With some smaller projects it may add far more than what is needed but better 
to have more and not use them, than not enough and need them, or at least that's what my Mother used to tell me :)

Fairly straightforward SCSS. Creates time-saving padding and margin helper classes for projects. Code is commented. Hope it helps!

Quick Example:
<pre>
&lt;section class="some-class"&gt;
  &lt;div class="some-other-class"&gt;
    @CONTENT
  &lt;/div&gt;
&lt;/div&gt;
</pre>

Rather than adding:
<pre>
.some-class {
  padding-top: 30px;
  padding-left: 20px;
  padding-right: 10%;
  padding-bottom: 0;
}
@media (min-width: 767px) {
  .some-class {
    padding-top: 5%;
    padding-bottom: 20px;
  }
}
.some-other-class {
  padding-left: 20%;
  padding-right: 2px;
}
</pre>

You could just use some of the generated classes from this code.

<pre>
&lt;section class="some-class pt-30 pl-20 pr-pct-10 pb-0 pt-xs-pct-5 pb-xs-20"&gt;
  &lt;div class="pl-pct-20 pr-2"&gt;
    @content
  &lt;/div&gt;
&lt;/section&gt;
</pre>

Is it the prettiest? Nope. Does it work and save time? Absolutely!
