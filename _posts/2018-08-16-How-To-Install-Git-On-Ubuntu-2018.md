---
layout: post
title: How To Install Git Version Control Systems On Ubuntu 2018 
comments: true

---
![Githublogo](https://raw.githubusercontent.com/mrayoung/ayoungnotes.github.io/master/_posts/img/octocat_kenobi.jpg)
Git Version control systems is my favorite share and collaborate coding projects. Not just me Git is one of the most popular version control.

Further than my noted I will show the step installing and configuring Git on an Ubuntu 18.04 and this could be available to any version of Ubuntu.

### Step 1 — Update Default Packages
Logged into your Ubuntu 18.04 server as a sudo non-root user, first update your default packages.

sudo apt update

### Step 2 — Install Git
sudo apt install git

### Step 3 — Confirm Successful Installation

You can confirm that you have installed Git correctly by running this command and receiving output similar to the following:

git --version
Output
git version 2.17.1

### Step 4 — Set Up Git
Now that we have Git installed and to prevent warnings, you should configure it with your information.

git config --global user.name "Your Name"
git config --global user.email "youremail@domain.com"
If you need to edit this file, you can use a text editor such as nano:

nano ~/.gitconfig
~/.gitconfig contents
[user]
  name = Your Name
  email = youremail@domain.com


This is should be working, if you found any issue please let's me know on below comment.

<div id="disqus_thread"></div>
<script>

/**
*  RECOMMENDED CONFIGURATION VARIABLES: EDIT AND UNCOMMENT THE SECTION BELOW TO INSERT DYNAMIC VALUES FROM YOUR PLATFORM OR CMS.
*  LEARN WHY DEFINING THESE VARIABLES IS IMPORTANT: https://disqus.com/admin/universalcode/#configuration-variables*/
/*
var disqus_config = function () {
this.page.url = PAGE_URL;  // Replace PAGE_URL with your page's canonical URL variable
this.page.identifier = PAGE_IDENTIFIER; // Replace PAGE_IDENTIFIER with your page's unique identifier variable
};
*/
(function() { // DON'T EDIT BELOW THIS LINE
var d = document, s = d.createElement('script');
s.src = 'https://https-www-ayoungnotes-com.disqus.com/embed.js';
s.setAttribute('data-timestamp', +new Date());
(d.head || d.body).appendChild(s);
})();
</script>
<noscript>Please enable JavaScript to view the <a href="https://disqus.com/?ref_noscript">comments powered by Disqus.</a></noscript>

<script id="dsq-count-scr" src="//https-www-ayoungnotes-com.disqus.com/count.js" async></script>
