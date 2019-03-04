---
layout: post
author: elsa
title: Creating my github.io using Jekyll, from start to finish.
---

<div class="container">
<h2><a href="{{ site.baseurl }}{{ page.url }}">{{ page.title }}</a></h2>

<p>
    Creating this website was my very first web dev (web development) project. Since starting this project there has been a slew of language formalities I've had to learn, kinks I've had to figure out, and choices I've had to make. Halfway through the process, I decided to document it. I wanted to provide an extra resource to students and developers building their own github.ios using Jekyll. I hope you find this post useful.
</p>

<p>
    This website is hosted by <a href="https://pages.github.com/">GitHub Pages</a>. A GitHub Page turns a GitHub repository into a site with the extension github.io. Between WordPress and GitHub Pages, I chose github.io because it <i>seemed</i> simpler and more doable. GitHub Pages mentioned using <b>Jekyll</b>, a <a href="https://www.quora.com/How-does-a-static-site-generator-like-Jekyll-work">static site generator</a>, so I gave it a shot. A static site generator, sometimes called a flat page or stationary page, is said to require no PHP scripting, no databases, nor server code. It is therefore safer, but less interactive. For more on Jekyll, scroll down to find the section <b>Choosing Jekyll</b>.
</p>

<p>
    Like for all other projects:
    <ul>
        <li>I used original docs (documentation) and guides, like <a href="https://help.github.com/en/categories/github-pages-basics">GitHub Pages Basics</a> and <a href="https://jekyllrb.com/docs/">Jekyll Docs</a></li>
        <li>I found a lot of answers on Stack Overflow.</li>
        <li>I had to be be flexible. Some of the googled solutions did not work for me, so I played around with the code.</li>
        <li>I looked at example Jekyll projects + code.</li>
    </ul>
</p>


<h1>Downloading the newest version of Ruby for macOS using Homebrew</h1>
<p>
    To use Jekyll I had to download the newest version of Ruby.

    I spent hours trying to figure out how to change a PATH so ruby would default to the new, freshly downloaded version.

    The <a href="https://stackoverflow.com/questions/54471291/how-to-use-the-homebrews-ruby-package-instead-of-the-ruby-package-that-comes-wi">solution</a> ended up being:

    <script src="https://gist.github.com/elsajyang/842891a8298462dae92b2ea2e1460084.js"></script>

    The two other popular options for managing ruby and its many versions is to use <i>rvm</i> or <i>rbenv</i>. After my struggle, I ended up downloading rvm anyway.
</p>

<h1>Choosing Jekyll</h1>
<p>
    I chose Jekyll because it was cofounded I probably should have done some more research as to I would have followed this [Youtube video](https://www.youtube.com/watch?v=BA_c3bGQXlQ) to at least publish a testing page using a Jekyll theme.

    Up to this point I only know how to make edits, code, and deploy in a Jekyll workflow setting as insane as it is.
</p>






# Resources
* [How Jekyll, a static site generator, works. **Quora**.](https://www.quora.com/How-does-a-static-site-generator-like-Jekyll-work)
* [Updating Ruby: How to add to a Path to ~/.bash_profile](https://stackoverflow.com/questions/54471291/how-to-use-the-homebrews-ruby-package-instead-of-the-ruby-package-that-comes-wi)

</div>
