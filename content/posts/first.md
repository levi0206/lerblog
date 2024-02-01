---
title: "How to Build your Website Using Hugo on GitHub Pages: Summary "
date: 2024-02-01T10:04:47+08:00
draft: false
---
Hugo is a fast and modern static site generator that makes building website much easier. With Hugo, you can host your beautiful website on GitHub Pages, Netlify or other platforms.
## Create a Hugo blog
Before we start, please make sure your hugo is installed. You can check your hugo version by typing 
```
hugo version
```
at your terminal. Next, go to the directory that you want to store website 
```
cd Home
```
for example, and run
```
hugo new site testhugo
```
This command fetches a site template but no content or theme yet. Next, choose your favorite theme and install it. In my case, I choose [PaperMod](https://github.com/adityatelange/hugo-PaperMod) as my theme. For PaperMod, you can install by
```
cd testhugo
git clone https://github.com/adityatelange/hugo-PaperMod themes/PaperMod --depth=1
```
and set theme in `hugo.yaml` (or `.homl` similarly but make sure your syntax is correct)
```
theme: PaperMod
```
To check your website, type 
```
hugo server
```
at your terminal, and you should be able to see
```
Web Server is available at http://localhost:1313/ (bind address 127.0.0.1)
```
It is a local server that dynamically updating your changes on local device. If you want to check how your website looks like, you can turn on `hugo server` and editor at the same time. **However, if your website does not show, you can erase** `baseurl` in your `hugo.yaml` **by setting**
```
baseurl: ""
```
At least for, I can see my website using this trick.

## Custom layout


# References
- Installation
    - Install Hugo: https://gohugo.io/installation/
    - Install PaperMod: https://github.com/adityatelange/hugo-PaperMod
    - Hugo quickstart: https://gohugo.io/getting-started/quick-start/
    - Helpful YouTube video: Create A Blog WIth Hugo And Deploy To Github In 10 Minutes, [link](https://www.youtube.com/watch?v=psyz4UPnGAA)
    - Helpful YouTube video: Getting Started With Hugo | FREE COURSE, [link](https://www.youtube.com/watch?v=hjD9jTi_DQ4&t=2299s)
- Debugging:
    - Problems `fatal authentication` for git push:
        - GitHub documentation: https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/managing-your-personal-access-tokens
        - Helpful YouTube video: How to fix 'fatal authentication failed for git push' permanently, [link](https://www.youtube.com/watch?v=pHaZW9OWUAQ)

### Device
ubuntu, linux, 22.04