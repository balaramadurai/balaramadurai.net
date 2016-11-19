+++
tags = ["hugo","git","github","hosting","free","orgmode"
]
categories = ["learning"
]
date = "2016-11-17T09:43:47+05:30"
title = "How I Re-setup My Blog and Website using Hugo, Github and a Green Screen"
banner = "/img/my-blog-website.jpg"
+++

![My Website and Blog](/img/my-blog-website.jpg "My Website and Blog")  
*My Website and Blog*

Wordpress.com and self-hosted wordpress.org are very nice and easy to setup. I helped my wife [aladybird](https://twitter.com/aladybirdblogs) setup
her travelog website - [funderfulworld.com](http://funderfulworld.com) on a self-hosted wordpress.org installation. However, there is a big problem that I faced when it came to
Wordpress installations. 

They are CPU hungry. 

If you are paying for the hosting then there sure is no problem, since you get unlimited CPU
time. However, if you are a cheapy like me, then the free hosting sites scowl at you thrice and throw you out like an uninvited guest. All I did was
to devour some of their CPUs by adding a few harmless plugins to my Wordpress installation.

*Pssst...* You can try [sandstorm.io](http://sandstorm.io) and install a Wordpress "grain" though. But you get sucked into this quagmire of CNAME and
 A record stuff. I got lost trying to do that.

## Enter and Exit the Github

I looked high and low for a reliable **free** hosting service provider and came across [Github](https://en.wikipedia.org/wiki/GitHub). Now, Github is like UNIX of the yesteryears and Linux of
the current generation. As the saying goes,

> UNIX is user friendly, but it is careful in choosing it's friends.

Same can be said about Github. My head reeled from phrases like "init", "commit", "clone" and the likes. I steered clear from github for a while. 

## Enter Org Mode

Apart from being a nerd, I am also a productivity freak. I looked high and low for a productivity package that was simple to use and was powerful to
keep tweaking forever. I tried a whole host of apps and software trying to be productive and organized. Finally, I hit upon Gina Tripani's
[todo.txt](http://todotxt.com/). However, it lacked a reminder system or atleast I couldn't figure out how to get the reminder system going.

I got sucked into this whole simplicity part of the todo system. A few reddits later, I came to
[orgmode.org](http://orgmode.org). It said something about an editor called Emacs. It brought back some pleasant memories from the past, about 20 years ago, when I used
emacs to play snake in text form in IIT, Madras. Oh those green screen days!!! 

I thought to myself that this could be a trip down the memory lane and I installed emacs and I prepped myself for org mode. A year later, I have still
been using org mode, which is an incredible feat on its own. It retained my interest for a year. I got comfortable with git through org mode. Long
story short - it was not as difficult as I thought it would be. 

Ok, now to the main topic of my post (after 4 years of no blogging):

## How to setup your blog and website for free using a custom domain name

Here are some of the steps that I went through to setup my website on [http://balaramadurai.net](http://balaramadurai.net)

1. First, sign up on [github](http://github.com/join) for a free account.
2. Create a repository and call it - ```< username >.github.io```  
For example, my repository is called ```balaramadurai.github.io```
3. Next download and install github GUI. I am on Windows 10, so I downloaded the [windows version](https://github-windows.s3.amazonaws.com/GitHubSetup.exe).   
Note - Alternatively, you can start with installation of Github GUI and create your repository there.
4. Next, download Hugo[^1] from the [website](http://gohugo.io). If you are on Windows, here is the
   [link](https://github.com/spf13/hugo/releases/download/v0.17/hugo_0.17_Windows-32bit.zip) that will help you.  
   Note - Extract the zip file and rename the ```hugo_****.exe``` to ```hugo.exe```. This will make your life a lot easier.
5. Look through the themes that they have and choose one for yourself.   
I found [this setup](https://gohugo.io/overview/quickstart/) guide useful. I chose [hugo-universal-theme](https://github.com/devcows/hugo-universal-theme) since they have a blog and a single page front page. They also have other bells and whistles, but you can very easily disable or enable them in config.toml.
6. Setup the hugo website and the test server. Here you will need the dreaded command line interface ```cmd``` from Win-R or Windows Run.  
Type ```hugo server -w``` and hit Enter.
7. Point your browser to ```localhost:1313``` and you will have a website running.
8. Copy the config.toml file from the theme to your main website folder, ```balaramadurai.net/``` folder in my case.
9. Changing content may be a bit involved. Look for ```img``` folder where your images are present and data where the nick nacks are present.[^2]
10. What you need to be changing according to the templates is the yaml files. Add as many as you want and change the content in those yaml files.
11. You will need to learn [Markdown format](https://daringfireball.net/projects/markdown/syntax) for writing your blog posts and all your posts will have a .md extension
12. Lastly run ```hugo``` in the same folder as your website and all your content is now ready to be githubbed.
13. By default, your entire website is present in the ```public``` folder. Copy all these files present inside the folder to the folder that has the
    github repository.
14. In the Github application, click on "Changes" tab and write a few lines in the "summary" and "Description" areas.
Note - One last thing before you push your website to production. Add a file called CNAME for custom domain name. In the contents of the file, enter
your domain name. In my case, it is ```balaramadurai.net```. If you don't want a custom domain name (I wonder why), your website is ready on ```http://<
username >.github.io```
15. Push the "Commit to Master" button.
16. Once that is done, click on the sync button

You are all set, your website is up and running.

You can jazz up your website by adding code from [sumome.com](http://sumome.com) which gives you things like contact forms, newsletter signups and social media share
buttons.

Have fun!!!

If you have any questions, please leave me a comment below and I'll try my best to help you.

[^1]: Hugo is the static website generator or the stuff that takes your mind off databases and javascript and all that

[^2]: I used a logo maker for my dr. bala ramadurai logo - [logo maker](https://logomakr.com/) and a [favicon generator](http://www.favicon-generator.org/search/---/B)
