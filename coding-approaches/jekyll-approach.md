# Jekyll Approach

Finished Example [Website](https://katherinemichel.github.io/self-hosted-church-website-jekyll) and [Code](https://github.com/KatherineMichel/self-hosted-church-website-jekyll/tree/gh-pages)<br>
Compare to the original [Squarespace website](http://www.prettyprairieumc.org)

## Background

[Jekyll](https://jekyllrb.com) is a web development framework invented at GitHub, the most popular place in the world for hosting open-source code. Jekyll sites can be hosted for free at GitHub, and can use a custom domain. Jekyll is very popular because it combines powerful web development options with free, easy deployment. 
 
## Cost Comparison

Squarespace
* $144/year basic, custom domain included
* Cost of labor, if any

Jekyll Site
* Free to host
* Cost of domain (~$10)
* Cost of labor, if any

## Tools Needed

* [Jekyll](https://jekyllrb.com)
* [Start Bookstrap Unstyled Starter Templates](http://startbootstrap.com/template-categories/unstyled)
* GitHub personal or organizational account, in order to use GitHub gh-pages
* Optional: CNAME file (for custom domain)
* Optional: [Disqus](https://disqus.com) (for blog post comments)

## Staged Deployment

In a mission critical, live production environment, a website may be viewed locally, before code changes are pushed to a web host and viewed on a staging site that is virtually the same as the production site. If the result on the staging site is satisfactory, the change may be pushed to the live site where it will be seen by users. A Jekyll site hosted through GitHub gh-pages does not offer an obvious staged deployment option like this. It is assumed that a site made using the approach in this GitBook will be simple/low traffic enough that updates could be verified locally and pushed directly to gh-pages. 

## Administration

Any person making updates to the site will need to have a personal GitHub account. The Jekyll site can be hosted through a personal GitHub account or through an organizational account. People who are members of an organization account will have special admin privileges. Non-members can submit changes to the site (not likely to occur for a small project), but an organization member will need to review the change before merging it with the code-base, or rejecting it. 

It is expected that the part of this website that would be updated most often would be the blog. Updating the blog is as simple as creating a word document, writing some text and saving it. Here are the steps: 
