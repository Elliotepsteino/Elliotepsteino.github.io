# Creating your own personal website using Jekyll and Github Pages

This meant as an end-to-end guide for the steps I took to create a [personal website](https://elliotepsteino.github.io/) using **Jekyll** and **Github Pages**, with the design source code based on an existing repo by [Leonid Keselman](https://github.com/leonidk). 

All the commands are based on MacOS. 

Please respect copyright of images and pdfs material in from this and other repos. 

I looked around a bit for other approaches to create a personal website but this worked well for me because:
1. You don’t need to buy a domain to host the website, you simply create a repo on github that hosts the website for you. If your Github username is, say, elliotepsteino, your website will be hosted in the domain: https//:elliotepsteino.github.io.
2. By using github pages, you can easily find source code from other people’s websites and fork their repo, this allows you to focus on the content you want to put on the site rather than the design.
3. Jekyll is a static site generator that works very well for Github websites. 

# Setup Jekyll:

To install Jekyll, you need [Rust](https://www.rust-lang.org/). This is a great guide for how to properly set up Rust: https://www.moncefbelyamani.com/how-to-install-xcode-homebrew-git-rvm-ruby-on-mac/. 

With rust installed, Jekyll is installed simply with 
```
gem install jekyll
```

# Website Design
The next step is to find a website design you like. I will base the rest of the guide on the design I used, which is a small modification of Leonid Keselman's [github repo](https://github.com/leonidk), who based his design on [Jon Barron’s site](https://jonbarron.info/). Another popular design is the Jekyll theme [Minimal](https://github.com/pages-themes/minimal) as well as [Minima](https://github.com/jekyll/minima).

The source code for my site https://elliotepsteino.github.io/ is at: https://github.com/Elliotepsteino/Elliotepsteino.github.io. 

To use the repo, just fork https://elliotepsteino.github.io/ or https://github.com/leonidk and name it yourusername.github.io.

You can then clone it:

```
git clone https://github.com/yourusername/yourusername.github.io.git
cd yourusername.github.io
```

You can now view the website locally at http://127.0.0.1:4000 by running
```
jekyll serve
```
Inside the yourusername.github.io directory.
# Adding Content
To add your own content, just remove the information from the other person, and add your own. 

Files to change:
_layout/default.html: This is the main page for the website, all posts and links social media etc. are added here. 
_posts/: This directory contains the posts for each entry displayed on your main page
_config: Basic configs, like your name, and google analytics tag. 

Replace the images in the /image folder rather than in /tn/images. The images in /tn/images are small, resized images generated by running the script 
```
bash ./_make_thumbnails.sh
``` 
If you get an error message that ‘convert’ is not installed when running the scirpt, first run
``` 
brew install imagemagick
```
To generate a new favicon (small icon on the tab), run  
```
bash ./_make_favicon.sh
```
Do not edit anything in the _site folder, this is an automatically generated folder that will be overwritten. 


Once you like the local version, in the yourusername.github.io folder, you can push it online!
From the website folder, run:
```
git add .
git commit -m “your commit message”
git push 
```
After 10 minutes, you should be able to see your website at https://yourusername.github.io/. 

## Other Notes
* There are fours categories of posts, so changing sizing requires edits in multiple paces.

* If you thought this was useful, consider linking to this repo or [my site](https://elliotepsteino.github.io/) as well as [Leonid Keselmans site](https://leonidk.com/)/[repo](https://github.com/leonidk).