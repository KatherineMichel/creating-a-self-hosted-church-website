# Jekyll Approach

Finished Example [Website](https://katherinemichel.github.io/self-hosted-church-website-jekyll) and [Code](https://github.com/KatherineMichel/self-hosted-church-website-jekyll/tree/gh-pages)<br>
Compare to the original [Squarespace website](http://www.prettyprairieumc.org)

## Background

[Jekyll](https://jekyllrb.com) is a static web development framework created at [GitHub](https://github.com), the most popular place in the world for hosting open-source code. Jekyll sites can be hosted for free at GitHub, and can use a custom domain. Jekyll is very popular because it combines powerful web development features with free, easy deployment. However, Jekyll is a framework for static sites (as opposed to dynamic) and does not offer all traditional web development functionality. Whether it is right for a specific project needs to be evaluated on a case-by-case basis. 
 
## Cost Comparison

Squarespace
* $144/year basic, custom domain included
* Cost of labor, if any

Jekyll Site
* [Free to host on GitHub](https://help.github.com/articles/using-jekyll-as-a-static-site-generator-with-github-pages)
* Cost of domain (~$10)
* Cost of labor, if any

## Tools Needed for This Project

* [Jekyll](https://jekyllrb.com)
* [Start Bookstrap Unstyled Starter Templates](http://startbootstrap.com/template-categories/unstyled)
* GitHub personal or organizational account, in order to use GitHub gh-pages
* Optional: CNAME file (for custom domain)
* Optional: [Disqus](https://disqus.com) (for blog post comments)

## Staged Deployment

In a mission critical, live production environment, a website may be viewed locally, before code changes are pushed to a web host and viewed on a staging site that is virtually the same as the production site. If the result on the staging site is satisfactory, the change may be pushed to the live site where it will be seen by users. A Jekyll site hosted through GitHub gh-pages does not offer an obvious staged deployment option like this. It is assumed that a site made using the approach in this GitBook will be simple/low traffic enough that major updates could be verified locally and pushed directly to gh-pages. Minor changes, such as adding a blog post, could be completedly directly in GitHub in the browser. 

## Administration

Any person making updates to the site will need to have a personal GitHub account. The Jekyll site can be hosted through a personal GitHub account or through an organizational account. If the site is hosted through a personal GitHub account and someone else makes a contribution to the site (a pull request), the account owner will review the contribution before merging it with the code-base, or rejecting it. If the site is hosted through an organizational account and a non-member (of the organization) makes a a pull request, a member of the organization account who has special admin privileges will review the contribution before merging or rejecting it. Code contributions are not likely to occur on a small project. 

It is expected that the part of this website that would be updated most often would be the blog. Updating the blog is as simple as creating a word document, writing some text and saving it. Here are the steps: 

Click on the _blog folder to open it

Copy the contents of the blog post template

Click the "Create new file" button in the upper right

When the file opens, paste the contents of the blog post template into the new file

In the "Name your file" box, type the date and blog post title with hyphens (exclude other punctuation such as apostrophes) followed by .markdown

Replace the generic "Front matter," with the information for this blog post (for example: title)

Under the "Front matter," type or copy and paste your blog post text

When you are happy with your post, scroll to the bottom of the page and click the green "Commit new file" button

The post will automatically populate on the blog homepage with a link to a blog post page
