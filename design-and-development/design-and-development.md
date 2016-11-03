# Design and Development

## Design

Website design is created by using [Hypertext Markup Language](https://en.wikipedia.org/wiki/HTML) (HTML) and [Cascading Style Sheets](https://en.wikipedia.org/wiki/Cascading_Style_Sheets) (CSS). I will be using a very popular and useful web development tool called [Bootstrap](http://getbootstrap.com). Bootstrap is a pre-made web development library for responsive design (design that automatically adapts to fit the browser size) and is used by many people around the world. I will be using several [unstyled starter Bootstrap templates](http://startbootstrap.com/template-categories/unstyled) from a website called [Start Bootstrap](http://startbootstrap.com). 

The templates I will be using will be: 
* Homepage: [Start Bootstrap 3 Col Portfolio](http://startbootstrap.com/template-overviews/3-col-portfolio)
* Homepage detail page and about page: [Start Bootstrap Portfolio Item](http://startbootstrap.com/template-overviews/portfolio-item)
* Activity page: a combination of pieces from other templates
* Blog homepage: [Start Bootstrap Blog Home](http://startbootstrap.com/template-overviews/blog-home)
* Blog post: [Start Bootstrap Blog Post](http://startbootstrap.com/template-overviews/blog-post)

## Development

Jekyll version of the self-hosted [church website](https://katherinemichel.github.io/self-hosted-church-website-jekyll) and [code](https://github.com/KatherineMichel/self-hosted-church-website-jekyll/tree/gh-pages)<br>

### Primary File Structure

    _includes/
           footer.html
           head.html
           header.html
    _layouts/
           default.html
           page.html
           post.html
    _posts/
           2016-07-11-pastors-welcome.markdown
           example.markdown
           yyyy-mm-dd-post-template.markdown
    css/
           bootstrap.css
           bootstrap.min.css
           main.css
    detail-pages/
           childrenandyouthministries.md
           church.md
           communityoutreach.md
           globalchurch.md
           musicministry.md
           prettyprairie.md
           unitedmethodistwomen.md
           welcome.md
           worship.md
    fonts/   
           glyphicons-halflings-regular.eot
           glyphicons-halflings-regular.svg
           glyphicons-halflings-regular.ttf
           glyphicons-halflings-regular.woff
    images/
           adult-choir.jpg
           childrens-choir.jpg
           church-outside-large.jpg
           church-outside.jpg
           church-sanctuary.jpg
           gretas-dog.jpg
           musicians.jpg
           rethink-church-logo.jpg
           stained-glass-window.jpg
           sunflowers.jpg
           thanksgiving-service.jpg
           umw-mission.jpg
           umw.jpg
           welcome-sign.jpg
    .gitignore
    README.md
    _config.yml
    about.html
    activities.html
    blog.html
    feed.xml
    index.html


