---
title: "Starting a Blog With Hugo"
date: 2019-06-20
draft: false
showSummary: false
---

I've had a blog for multiple years, but I found it difficult to put anything on it -- my inner critic has never been easy on me. Perfectionism can be hard to deal with. I also made the previous blog look really good, with high res images which made the site take longer to load, and made messing with the site's layout and design a really good way to distract myself from what was actually important: the writing. After a few years of hosting that blog I realised how little I was actually doing with it, so I decided not to renew. But, here we are. What changed?

I still wanted to have a blog, a place of my own that I could write on, and I stumbled on someone's blog which had a layout I really liked. I decided to email the guy, see how he was hosting [his blog](https://nomasters.io/) (he is a developer, they tend to have their ways) and he was really kind to tell me how to setup a blog on this platform called [Hugo](https://gohugo.io/). There's a few great reasons to use it and a few drawbacks depending on what you want to get out of your site:

1. It's cheap: other than the custom domain name (which costs maybe 10 to 20 bucks a year) and granted you're not an ultra popular blogger with a lot of heavy content (videos, images, etc.) on the site, multiple platforms will host your site for free, and without ads. Completely free.

2. It's ultra fast: Wordpress is software that makes creating websites easy, which means you can easily add dynamic content (user accounts, shopping, analytics, etc.) to your website using plugins. The fact that it's software plus dynamic plugins means that a site with Wordpress takes a lot longer to load, it needs to be updated frequently, and you need to login to Wordpress any time you want to add content. Hugo circumvents all of these things because it only generates static pages, meaning that there is no software, no databases, just individual pages with static content, which takes less time to load than it takes to type google.com in your web browser.

3. It's fun: with Hugo, creating a website is not the easiest if you don't know anything about coding. It actually took me multiple days and hours a day to set up the site you see right now. Depending on how much you like learning new things, and are willing to get stuck at certain points, googling solutions until you find someone who had the same problem you did and got it fixed (and so far I haven't had a problem which wasn't encountered before). 

There's actually relatively little coding involved, but in order to publish posts on the site, you need to know some [git](https://rogerdudler.github.io/git-guide/) and in order to make your posts look nice (such as the links and the bullet point lists you see here) you need to know [Markdown](https://www.markdownguide.org/). 

Then, if you want to change the look of the site, there are pre-configured themes that you can install easily, but if you want to really customise it to your own liking, you need to know at least the basics of HTML and CSS. If you're already at that stage, Hugo is easy, if you're not but willing to learn, it's a lot of fun.

Here's how it works: Instead of writing a blog post in Wordpress, in Word or in Medium, you create a markdown (.md) file in a program like Visual Studio Code, and write your post in there. 

When you're finished, you save the changes in that text file and _commit_ the changes you made (basically a double save). After you've committed the change, the file is now saved in your website, which is completely stored in a folder on your computer (Hugo is the framework that created that folder). 

Then you need to send the changes to the exact copy of your folder stored online in Github. Then, depending on which hosting platform you choose (Amazon Web Services and Netlify are popular, I'm using the latter) you link that online folder to the platform, which will then _deploy_ that folder to your custom domain, and any time you send any changes online, that platform will notice the changes and deploy them to your website.

If that is hard to follow, don't worry, it took me some time to figure out how it worked. I've figured out the basic things so far, although I want to customise my blog a bit more, and if possible add a way for people to get blog posts delivered to their email address.

I hope to post much more often on this blog. Check back soon!
