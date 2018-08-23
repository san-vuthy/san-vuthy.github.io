---
layout: post
title: How To Install Upgrade Kernel On Ubuntu to Latest Stable Kernel
comments: true

---
![Githublogo](https://raw.githubusercontent.com/mrayoung/ayoungnotes.github.io/master/_posts/img/kernel14184.png)
To keep the Kernel or our Linux system up-to-date is very important because the new technology is coming out very quickly. Upgrade our kernel will help our Linux device or system to recognize very easily and protect our system from vulnerabilities that has found from our previous versions.

Sound so interesting right? There is more I have a very basic bash script that will do all the thing for you to upgrade your kernel in following step.

### Step 1: Check Installed Kernel Version
In order to see the current version of our kernel we can type:
`$ uname -sr`

You should have the information about your kernel version.
After you see the current kernel then compare it with this site [Kernel.org](https://www.kernel.org)

If you are behind the latest kernel then we begin the step 2.

### Step 2: Upgrading Kernel
I hosted my script in github if you haven't install git in your system yet I recommend you check and follow the step here [How To Install Git Version Control Systems On Ubuntu 2018](https://www.ayoungnotes.com/2018/08/How-To-Install-Git-On-Ubuntu-2018)

Then clone all my script from my github repository in the following command:
`git clone https://github.com/mrayoung/Script.git`

If you only need a single script for your kernel upgrade just use WGET by following command:
`wget https://github.com/mrayoung/Script/blob/master/upgrade-ubuntu-kernel.sh`

If you clone from my repo need to go inside the directory and begin step 3.

### Step 3: Change Permission
Before execute the script you need to change to permission on script you want to executed this done by following command:
`chmod +x upgrade-ubuntu-kernel.sh`

### Step 4 — Execute Command for Upgrading
If you understand the bash or it's very easy to understand first it's make a directory.
next it's download all the deb file into that directory and last it's install by using`dpkg -i`.

To execute the script just type:
`sudo ./upgrade-ubuntu-kernel.sh` 

Then it's do the rest for you what I have mentioned above.

If take sometime you might need a cup of coffee if your internet connection is not very good.
after successfully executed you should reboot your system.

### Step 5 — Verify
Surely will need to verify your kernel after upgraded.
this is very easy just go back to Step 1. 
`$ uname -sr`

Let's me know if you find some error on your upgrading.

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
