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
    This website is hosted by <a href="https://pages.github.com/" target="_blank">GitHub Pages</a>. A GitHub Page turns a GitHub repository into a site with the extension github.io. Between WordPress and GitHub Pages, I chose github.io because it <i>seemed</i> simpler and more doable. GitHub Pages mentioned using <b>Jekyll</b>, a <a href="https://www.quora.com/How-does-a-static-site-generator-like-Jekyll-work" target="_blank">static site generator</a>, so I gave it a shot. A static site generator, sometimes called a flat page or stationary page, is said to require no PHP scripting, no databases, nor server code. It is therefore safer, but less interactive. For more on Jekyll, scroll down to find the section <b>Choosing Jekyll</b>.
</p>

<p>
    Like for all other projects:
    <ul>
        <li>I used original docs (documentation) and guides, like <a href="https://help.github.com/en/categories/github-pages-basics" target="_blank">GitHub Pages Basics</a> and <a href="https://jekyllrb.com/docs/" target="_blank">Jekyll Docs</a></li>
        <li>I found a lot of answers on Stack Overflow.</li>
        <li>I had to be be flexible. Some of the googled solutions did not work for me, so I played around with the code.</li>
        <li>I looked at example Jekyll projects + code.</li>
    </ul>
</p>
<br>

<h1>The Setup</h1>
<p>
    To build a github.io using Jekyll, you'll need the latest versions of:
    <ul>
        <li>Ruby</li>
        <li>Jekyll</li>
        <li>Bundler</li>
        <li>A text editor. <a href="https://code.visualstudio.com/" target="_blank">Visual Studio Code</a> for Mac has been one of my best recent downloads.</li>
        <li>A browser for localhost. This is for viewing an example of your site on your computer. I use Google Chrome.</li>
    </ul>
</p>
<br>

<h1>Downloading the newest version of Ruby for macOS using Homebrew</h1>
<p>
    To use Jekyll I had to download the newest version of Ruby. I spent hours trying to figure out how to change the PATH so Ruby would default to the freshly downloaded version. The <a href="https://stackoverflow.com/questions/54471291/how-to-use-the-homebrews-ruby-package-instead-of-the-ruby-package-that-comes-wi" target="_blank">solution</a> ended up being:
    <script src="https://gist.github.com/elsajyang/842891a8298462dae92b2ea2e1460084.js"></script>
</p>

<p>
    The two other popular options for managing ruby and its many versions are to use <i>rvm</i> or <i>rbenv</i>. After my struggle, I ended up downloading rvm anyway.
</p>
<br>


<h1>Some information about bash</h1>
<p>

<a href="https://www.quora.com/What-is-bash_profile-and-what-is-its-use" target="_blank">Quora answer</a>

Login Shells (.bash_profile)

A login shell is a bash shell that is started with - or --login. The following are examples that will invoke a login shell.

sudo su -
bash --login
ssh user@host
When BASH is invoked as a login shell, the following files are executed in the displayed order.

/etc/profile
~/.bash_profile
~/.bash_login
~/.profile
</p>
<br>


<h1>Choosing Jekyll</h1>
<p>
    I chose Jekyll because it seemed easy to use. <a href="https://en.wikipedia.org/wiki/Jekyll_(software)" target="_blank">Jekyll</a> was written in Ruby by GitHub's cofounder Tom Preston-Werner, so I thought it would work well in conjunction to this GitHub-oriented project. To use Jekyll, one must download Jekyll and bundler, which may also be a process of its own.
</p>

<p>
    For me, the Jekyll docs were not enough. My experience with Jekyll was more trial-and-error, meaning I playing around with the front matter and syntax, learning how files were being generated, etc. to debug. Truthfully, I probably should have done some more research, like watch <a href="https://www.youtube.com/watch?v=BA_c3bGQXlQ" target="_blank">a Youtube video</a> or read about other site testing systems. (I spent a long time trying to figure out why my edits off of a free Jekyll theme from <a href="http://jekyllthemes.org" target="_blank"></a> could not display correctly.) Meanwhile, the video shows how to, at the very least, publish a testing page using a Jekyll theme.
</p>

<p>
    The cool thing about Jekyll is it is a high level software. One can write a Markdown file and Jekyll will generate it into an HTML file for you. Editing and testing your site is also very user-friendly--simply edit the code, ensure there are no compilation errors,  type <code>jekyll serve</code> if not already serving, and refresh the <code>localhost:4000</code> page. There were really only two commands I was taught and therefore used, <code>jekyll build</code> and <code>jekyll serve</code>.
</p>

<p>
    Nevertheless, Jekyll is a pretty useful software for making sites. Unfortunately, I cannot compare it to other workflows, because at the time of writing, I know only how to make edits, code, and deploy in a Jekyll workflow setting.
</p>
<br>

<h1>Following the Jekyll docs as a start</h1>
<p>
    To learn the basics step by step, the <a href="https://jekyllrb.com/docs/" target="_blank">Jekyll Docs</a> worked well for me. I recommend following it to learn how to structure your files. You create an <code>index.html</code> file and learn the basic HTML file structure. You learn about <b>front matter</b>, a way to set variables of a file, sort of like an object and its instance variables. And you learn how to employ include and layout files.
</p>

<p>
Step by Step Takeaways
<ul>
    <li>html, mds are for content. index, about, navigation</li>
    <li>sites use layouts if pages share the same attributes. Layouts are used to avoid copying and pasting duplicate code. if all x pages of your site look the same, you can use a layout page. content is a special Jekyll variable that lives in the html body tag. it renders the content of the page's body it’s called on.</li>
    <li>this is where most of the ux/ui appearances layout edits are made</li>
    <li>Whereas layouts pertain to the whole placement of features on a page, includes allow us to create those repeated features. An example is a site's navigation or navigation bar.</li>
    <li>use includes if we want a page to include content from another file (don’t need to copy and paste, but the referencing does the copy and paste for us).</li>
    <li>includes are not supposed to have front matter.</li>
    <li>use data to separate content from source code. data probably changes a lot based on input, layouts change only to add new features and what not, includes don’t seem to change much</li>
    <li>YAML like <code>_config.yml</code></li>
    <li>In Jekyll, a file is a page on the site. so site.url, site.title to page.url, page.title</li>
</ul>
</p>

<p>
Errors
<ul>
    <li>When I made _layouts.default.html, I got 404 Not Found “/index.html” errors
    _config.yml page had a baseurl. 
    Set baseurl = “” at some point</li>
    <li>it was a mere “permalink: /posts” as opposed to “permalink: /posts/“. will kill someone.
    a bug. /foo.html => /foo, which wasn’t possible for me
    /foo/index.html =? /foo/ only this worked for me
    <a href="https://github.com/jekyll/jekyll/issues/6709" target="_blank">Permalinks</a></li>
</ul>
</p>
<br>

<h1>Adding a feature: creating a simple navbar with links</h1>
<p>
A <b>navbar</b> (navigation bar) allows a user to go from page to page on your site. When creating my site, I wanted a homepage, an about me page, and a page for posts. Ergo, I needed a navbar. To create a navbar, I need to:
<ul>
    <li>Determine which pages the navbar will appear. Since its a navbar, it will appear on nearly all my pages.</li>
    <li>Since it is a repeated feature, I create new include navbar.html file in incldes folder. Its a feature that will be reused over and over again</li>
    <li>I only have two types of layouts, default and posts. I will add an include line on both.</li>
    <li>Figure out where the navbar will appear on a page. Since its a navbar, it will conveniently always appear at the very top of my page, so I add it to the beginning of my html body tags in the layouts default and posts. (Of course, if this were some other feature, that might not be the case.)</li>
    <li>I have a data folder. I have a navigation.yml file in which I delineated all my links. So my _includes/navbar.html can use site.data.navigations</li>
    <script src="https://gist.github.com/elsajyang/828a80561b03ee118ddb51423a6559e6.js"></script>
    <li>Once all the data is available, I change the CSS. I make a new _navbar folder in _sass</li>
    <li>Lastly needed to change css/main.scss to import 'navbar'</li>
</ul>
</p>
<br>


<h1>Resources</h1>
<p>
<ul>
    <li><a href="https://www.quora.com/How-does-a-static-site-generator-like-Jekyll-work" target="_blank">How Jekyll, a static site generator, works. <i>Quora.</i></a></li>
    <li><a href="https://stackoverflow.com/questions/54471291/how-to-use-the-homebrews-ruby-package-instead-of-the-ruby-package-that-comes-wi" target="_blank">Updating Ruby: How to add to a Path to ~/.bash_profile. <i>Stack Overflow.</i></a></li>
    <li><a href="https://www.quora.com/What-is-bash_profile-and-what-is-its-use" target="_blank">What is bash profile and what is its use? <i>Quora.</i></a></li>
    <li><a href="https://en.wikipedia.org/wiki/Jekyll_(software)" target="_blank">Jekyll. <i>Wikipedia.</i></a></li>
    <li><a href="https://github.com/jekyll/jekyll/issues/6709" target="_blank">Jekyll Permalinks. <i>GitHub Help.</i></a></li>
</ul>
</p>

</div>
