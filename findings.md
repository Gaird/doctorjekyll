---
layout: default
title: "Jekyll Tests and Findings"
permalink: /findings
---

# Jekyll Tests and Findings

# Findings

- [Github Pages appears to have a more user-friendly/pre-packaged UI](https://pages.github.com/), though still CLI based
- [Github pages Jekyll themes built into Github](https://pages.github.com/themes/)
- [Kinsta article / How To run Jekyll locally on MacOS](https://kinsta.com/blog/jekyll-static-site/) (may be different than the Gitlab method right below. **↓**
- [Gitlab Pages article how to get started with a Jekyll site](https://docs.gitlab.com/ee/user/project/pages/getting_started/pages_from_scratch.html)

## Run Jekyll locally on MacOS

Ramp up and [test running Jekyll locally](https://kinsta.com/blog/jekyll-static-site/), which requires some CLI work on Sonoma, which runs an old version of Ruby that needs updating, but my Homebrew needs updating before I can do that. See screenshot below… <sigh>

### Things I Gotta Fix Before Running Jekyll Locally

![Image](/images/image.png)

Depending which article I am reading, there is one way to do a Jekyll local install as a straight up, running the site locally, for upload somewhere as a static site.

Vs. following [this article about running Jekyll locally when using Gitlab Pages](https://docs.gitlab.com/ee/user/project/pages/getting_started/pages_from_scratch.html), which runs a Docker image, uses Gemfiles and such. This may need Dimas to guide.

### Next Steps

Test Jekyll themes on Github pages

[Found this developer’s blog](https://aregsar.com/blog/2019/how-to-customize-your-github-pages-blog-style-in-five-minutes/) that explains some tips for customizing the Cayman theme on Github Page

Test Jekyll theme on Gitlab pages

## This Just In…

Found [this docs site for GitHub Developers](https://githubtraining.github.io/training-manual/#/01_getting_ready_for_class)

It has a very nice theme. I wonder what they use? Let’s view source:

![Image](/images/image-1.png)

Not sure what I am looking at. Let’s poke around. Firs the stylesheet link to

[https://unpkg.com/docsify/lib/themes/vue.css](https://unpkg.com/docsify/lib/themes/vue.css)

Not sure what this is, but then I check out

[https://unpkg.com/](https://unpkg.com/)

It is a CDN for NPM stuff, by Cloudflare. Not sure, will check back later.

Then I search up [Docsify](https://docsify.js.org/#/), and bingo, [this is the software](https://docsify.js.org/#/) used by the GitHub Dev docs site

It is [a no HTML page generator](https://docsify.js.org/#/?id=docsify), generates pages with JavaScript. Hm, ok, and it works on GitHub pages. Let’s check out how I can test it. I look at the Guide, and down on the Deploy tab I see instructions for running Docsify on various platforms and lo and behold, I see [instructions for GitLab pages](https://docsify.js.org/#/deploy), too.

Et voilà! That will be our next test.

![Image](/images/image-2.png)
