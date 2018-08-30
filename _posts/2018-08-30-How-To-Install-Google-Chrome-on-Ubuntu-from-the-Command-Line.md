---
layout: post
title: How To Install Google Chrome on Ubuntu from the Command Line
comments: true

---
![](https://raw.githubusercontent.com/mrayoung/ayoungnotes.github.io/master/_posts/img/chrome.png)

I have installed new Ubuntu Operating System on my laptop during the trip to ShenZhen. For those who never been here it's pretty easy to install Google Chrome by download its from Google website.

As everyone know very well that China is one of a very restricted Internet connect there is no google here. So it's a bit challenge to install Google Chrome here. There is another possible way to install Google Chrome and I decide to write an article for those who want to do it correctly.

Let's jumping to bellow step

### Step: 1 Add Source List

Press CTRL+ALT+T to open a terminal or you can open any terminal as your favorite once, then edit sources.list file with any favorite text editor I love Nano so i'm going to do with it. You should have done it with super user privilege.

`sudo nano /etc/apt/sources.list`

Use the down arrow key to scroll to the bottom of this file. Add the following APT line at the end of the file.

`deb [arch=amd64] http://dl.google.com/linux/chrome/deb/ stable main`

[www.ayoungnotes.com|Source List](https://raw.githubusercontent.com/mrayoung/ayoungnotes.github.io/master/_posts/img/chrome_source_list.png)

### Step: 2 Add Add Linux Signing Key

In Nano text editor in order to save the file we need to press Ctrl+O, then Enter to confirm. press CTRL+X to exit out of this file of you can make it's faster by CTRL + X and Enter. After that, enter the following command to download Google’s signing key.

`wget https://dl.google.com/linux/linux_signing_key.pub`

Then use `apt-key to add`  with sudo privilege to your keyring so the package manager can verify the integrity of Google Chrome package.

`sudo apt-key add linux_signing_key.pub`

### Step: 3 Install Google Chrome

Lets update package list before install the stable version of Google Chrome.

`sudo apt update`
`sudo apt install google-chrome-stable`

Installing Google Chrome browser on Ubuntu is pretty easy! As always, if you found this post useful or any error please let's me know on commend below.

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
