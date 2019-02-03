+++
title = "Hello, Hugo!"
subtitle = "About my decision to start blogging again. Now, with Hugo."

date = 2019-02-03
draft = false

# Authors. Comma separated list, e.g. `["Bob Smith", "David Jones"]`.
authors = ["Gabi Udrescu"]

summary = "First blog post with Hugo"

# Projects (optional).
#   Associate this post with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `projects = ["deep-learning"]` references 
#   `content/project/deep-learning/index.md`.
#   Otherwise, set `projects = []`.
# projects = ["internal-project"]

# Featured image
# To use, add an image named `featured.jpg/png` to your project's folder. 
# [image]
  # Caption (optional)
#  caption = "Image credit: [**Tenor**](https://tenor.com/view/cat-car-excited-smile-pet-gif-5570235)"

  # Focal point (optional)
  # Options: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight
#  focal_point = ""

  # Show image only in page previews?
#  preview_only = false

# Set captions for image gallery.

[[gallery_item]]
album = "gallery"
image = "https://media1.tenor.com/images/9123451f0b0d908cdc60dfa5fc9a36d5/tenor.gif?itemid=13366779"
caption = "Default"

[[gallery_item]]
album = "gallery"
image = "https://media1.tenor.com/images/2a5662a25de3a724f5ac08965d275233/tenor.gif?itemid=5734766"
caption = "Ocean"

[[gallery_item]]
album = "gallery"
image = "https://media1.tenor.com/images/119dd3797490c22e49cf42e5357fb719/tenor.gif?itemid=4233186"
caption = "Forest"
+++

<div class="tenor-gif-embed" data-postid="4481045" data-share-method="host" data-width="100%" data-aspect-ratio="1.9606299212598424"><a href="https://tenor.com/view/welcome-gif-4481045">Welcome Back - Despicable Me GIF</a> from <a href="https://tenor.com/search/welcome-gifs">Welcome GIFs</a></div><script type="text/javascript" async src="https://tenor.com/embed.js"></script>

{{% toc %}}

## **A bit of history**

Hello there! I haven't done this for a while now and I guess I've become a little bit rusty. I first started my blog in 2007, on Softpedia.com. It was a very popular forum back in the days, since Facebook was still young and the adoption in Romania was very low.

Soon after, I bought myself a domain and ended up wasting my teenager time on writing various stuff I was very proud of.

Even if now, thinking about it in retrospective, I realise that all that time could have been used for something else, _je ne regrette rien_, as it allowed me to learn a lot of stuff about how to build and maintain a website, be part of a community.

And I've also met hell lot of people. It was probably one of the best decisions I took. 

Fast forward a few more years, I decided that I have more important stuff to do instead of just write random thoughts on the internet. I began to read more and the more I read, the more I realised the little I know and felt that I should only start writting when I know enough.

I'm not saying that now I know everything (although, I do :smile:), but I feel more confident in publishing here bits of text.

## **Why Hugo**

One of the biggest drawbacks on restarting my blogging habbit was the idea that I have to maintain my own blogging infrastructure. Domain, server, PHP, MySQL, Wordpress, plugins, security updates, themes, customizations, scalability... all that made me reluctant on going down this path again.

I was always afraid that if I setup my own infrastructure on DigitalOcean it will never be good enough to keep my blog online on a big traffic spike. Nor it will be unhackable. 

I kinda overcame these fears, but still, too lazy to do it.

A few weeks ago I realised that lots of personal web pages are online through Jekyll and GitHub Pages and I started doing some research on static page builders served through serverless infrastructure.

And so I discovered [Hugo](https://gohugo.io/) and fell in love with the [Academic theme](https://sourcethemes.com/academic/) (I'm currently using, btw). It was the perfect setup for me - in terms of features.

Hugo was simple enough to allow me to bootstrap a blog, while geeky in the same time, keeping me interested. And having everything in plain text makes it really really really portable. 

## **Stack setup**

So, I have my domain using DigitalOcean DNS because, sometimes, when I'm doing some experiments, I want to have a public CNAME for that. The content is hosted on GitHub and deployment is handled automatically with Netlify.

Netlify is a CI/CD service, similar to Travis CI but better integrated with Hugo, doing a very good job for static websites. Less configuration to write than for Travis. 

Initially, I wanted to use Netlify CMS, a Javascript application that is offering a CMS interface for your github website repository, once you get everything up and running. 

But ended up using Sublime (at least for now).

## **How it works**

- create a folder
- create a file with .md extension
- copy the template from a previous post
- start writting
- check everything locally it works well
- git commit & git push

and in 30 seconds it's done. I have posted a new blog post or a modification to my website. 

## **Drawbacks**

Well, I have to manually add when the post was published. And I don't (yet) have fancy CMS, with WYSIWYG, powerfull galleries or various features that don't really matter.

You need to understand how Git works, if you don't want to use the edit screen in GitHub (that does not have autosave, like Wordpress).

And you don't have custom emails for your domain. Unless you use something like [ForwardEmail](https://forwardemail.net).

## **What do you have available to play with**

1. a personal website that I built in a couple of days, withouth writting a single line of code
1. a blog
1. with photo gallery
1. that I don't have to worry about hosting or technical infrastructure
1. that is not vendor locked
1. [I can do slides in plain text]({{< ref "slides/test">}})
1. I can announce [future events]({{< ref "talk">}}) I'm attending or that I'm organizing
1. I don't have to rely on 3rd parties I don't control in order to manage my online presence (LinkedIn, Facebook etc.)
1. a place where I can write tutorials 
1. something to brag about
1. a new toy I can play with
1. emojy :heart: :smile:

Speaking of gallery (confidently click one of the gifs below):

{{< gallery >}}

And code syntax highlighting:

```php

<?php

$foo = new Bar();

if($foo->isGreat())
{
  echo 'trully is great!'
}

```

```sql

select * from cms where type = 'static' and rating = 'awesome'

```

And social media posts updates:

{{< tweet 1087652274942431233 >}}


<!-- **Academic** makes it easy to create a beautiful website for free using Markdown. Customize anything on your site with widgets, themes, and language packs.

Follow our easy [step by step guide](https://sourcethemes.com/academic/docs/install/) to learn how to build your own free website with Academic. [Check out the personal demo](https://themes.gohugo.io/theme/academic/) or the [business demo](https://sourcethemes.com/academic/) of what you'll get in less than 10 minutes.

- [View the documentation](https://sourcethemes.com/academic/docs/)
- [Ask a question](http://discuss.gohugo.io/)
- [Request a feature or report a bug](https://github.com/gcushen/hugo-academic/issues)
- Updating? View the [Update Guide](https://sourcethemes.com/academic/docs/update/) and [Release Notes](https://sourcethemes.com/academic/updates/)
- Support development of Academic:
  - [Donate a coffee](https://paypal.me/cushen)
  - [Become a backer on Patreon](https://www.patreon.com/cushen)
  - [Decorate your laptop or journal with an Academic sticker](https://www.redbubble.com/people/neutreno/works/34387919-academic)
  - [Wear the T-shirt](https://academic.threadless.com/) It was

[![Screenshot](https://raw.githubusercontent.com/gcushen/hugo-academic/master/academic.png)](https://github.com/gcushen/hugo-academic/)

Key features:

- Easily manage various content including homepage, blog posts, publications, talks, and projects
- Extensible via **color themes** and **widgets/plugins**
- Write in [Markdown](https://sourcethemes.com/academic/docs/writing-markdown-latex/) for easy formatting and code highlighting, with [LaTeX](https://en.wikibooks.org/wiki/LaTeX/Mathematics) for mathematical expressions
- Social/academic network linking, [Google Analytics](https://analytics.google.com), and [Disqus](https://disqus.com) comments
- Responsive and mobile friendly
- Simple and refreshing one page design
- Multilingual and easy to customize

## Color Themes

Academic is available in different color themes and font themes.

{{< gallery >}}

## Ecosystem

* **[Academic Admin](https://github.com/sourcethemes/academic-admin):** An admin tool to import publications from BibTeX or import assets for an offline site
* **[Academic Scripts](https://github.com/sourcethemes/academic-scripts):** Scripts to help migrate content to new versions of Academic

## Install

You can choose from one of the following four methods to install:

* one-click install using your web browser (recommended)
* install on your computer using Git with the Command Prompt/Terminal app
* install on your computer by downloading the ZIP files
* install on your computer with RStudio

### Quick install using your web browser

1. [Install Academic with Netlify](https://app.netlify.com/start/deploy?repository=https://github.com/sourcethemes/academic-kickstart)
    * Netlify will provide you with a customizable URL to access your new site
2. On GitHub, go to your newly created `academic-kickstart` repository and edit `config.toml` to personalize your site. Shortly after saving the file, your site will automatically update
3. Read the [Quick Start Guide](https://sourcethemes.com/academic/docs/) to learn how to add Markdown content. For inspiration, refer to the [Markdown content](https://github.com/gcushen/hugo-academic/tree/master/exampleSite) which powers the [Demo](https://themes.gohugo.io/theme/academic/)

### Install with Git

Prerequisites:

* [Download and install Git](https://git-scm.com/downloads)
* [Download and install Hugo](https://gohugo.io/getting-started/installing/#quick-install)

1. [Fork](https://github.com/sourcethemes/academic-kickstart#fork-destination-box) the *Academic Kickstart* repository and clone your fork with Git: 

        git clone https://github.com/sourcethemes/academic-kickstart.git My_Website
    
    *Note that if you forked Academic Kickstart, the above command should be edited to clone your fork, i.e. replace `sourcethemes` with your GitHub username.*

2. Initialize the theme:

        cd My_Website
        git submodule update --init --recursive

### Install with ZIP

1. [Download](https://github.com/sourcethemes/academic-kickstart/archive/master.zip) and extract *Academic Kickstart*
2. [Download](https://github.com/gcushen/hugo-academic/archive/master.zip) and extract the *Academic theme* to the `themes/academic/` folder from the above step

### Install with RStudio

[View the guide to installing Academic with RStudio](https://sourcethemes.com/academic/docs/install/#install-with-rstudio)

## Quick start

1. If you installed on your computer, view your new website by running the following command:
      
        hugo server

    Now visit [localhost:1313](http://localhost:1313) and your new Academic powered website will appear. Otherwise, if using Netlify, they will provide you with your URL.
           
2. Read the [Quick Start Guide](https://sourcethemes.com/academic/docs/) to learn how to add Markdown content, customize your site, and deploy it. For inspiration, refer to the [Markdown content](https://github.com/gcushen/hugo-academic/tree/master/exampleSite) which powers the [Demo](https://themes.gohugo.io/theme/academic/)

3. Build your site by running the `hugo` command. Then [host it for free using Github Pages](https://georgecushen.com/create-your-website-with-hugo/) or Netlify (refer to the first installation method). Alternatively, copy the generated `public/` directory (by FTP, Rsync, etc.) to your production web server (such as a university's hosting service).

## Updating

Feel free to *star* the project on [Github](https://github.com/gcushen/hugo-academic/) to help keep track of updates and check out the [release notes](https://sourcethemes.com/academic/updates) prior to updating your site.

Before updating the framework, it is recommended to make a backup of your entire website directory (or at least your `themes/academic` directory) and record your current version number.

By default, Academic is installed as a Git submodule which can be updated by running the following command:

```bash
git submodule update --remote --merge
```

[Check out the update guide](https://sourcethemes.com/academic/docs/update/) for full instructions and alternative methods.

## Feedback & Contributing

Please use the [issue tracker](https://github.com/gcushen/hugo-academic/issues) to let me know about any bugs or feature requests, or alternatively make a pull request.

For support, head over to the [Hugo discussion forum](http://discuss.gohugo.io).

## License

Copyright 2016-present [George Cushen](https://georgecushen.com).

Released under the [MIT](https://github.com/gcushen/hugo-academic/blob/master/LICENSE.md) license. -->
