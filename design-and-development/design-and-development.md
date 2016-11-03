# Design and Development

Jekyll version of the self-hosted [church website](https://katherinemichel.github.io/self-hosted-church-website-jekyll) and [code](https://github.com/KatherineMichel/self-hosted-church-website-jekyll/tree/gh-pages)<br>

## Design

Website design is created by using [Hypertext Markup Language](https://en.wikipedia.org/wiki/HTML) (HTML) and [Cascading Style Sheets](https://en.wikipedia.org/wiki/Cascading_Style_Sheets) (CSS). I will be using a very popular and useful web development tool called [Bootstrap](http://getbootstrap.com). Bootstrap is a pre-made web development library for responsive design (design that automatically adapts to fit the browser size) and is used by many people around the world. I will be using several [unstyled starter Bootstrap templates](http://startbootstrap.com/template-categories/unstyled) from a website called [Start Bootstrap](http://startbootstrap.com). 

The templates I will be using will be: 
* Homepage: [Start Bootstrap 3 Col Portfolio](http://startbootstrap.com/template-overviews/3-col-portfolio)
* Homepage detail page and about page: [Start Bootstrap Portfolio Item](http://startbootstrap.com/template-overviews/portfolio-item)
* Activity page: a combination of pieces from other templates
* Blog homepage: [Start Bootstrap Blog Home](http://startbootstrap.com/template-overviews/blog-home)
* Blog post: [Start Bootstrap Blog Post](http://startbootstrap.com/template-overviews/blog-post)

## Development

### Code Explainer

The _config.yml file contains project configurations. The first file to be rendered is the index.html, which is the website homepage. When the website homepage URL is entered into a browser and the index.html file is fetched, or a hyperlink on the website is clicked and another corresponding .html page is fetched, based on the front matter in the .html file, a template is fetched from the _layouts folder. The content of the .html file is inserted into the template as content. Often, the template will indicate partial templates in the _includes folder (such as header and footer) to fetch and insert into the template where indicated.

The main website pages (Homepage (index.html), Activities, Blog, and About) use the default template. Blog posts inserted into the Blog page are found in the _posts folder and use the post template. 

The website Homepage contains rows of "cards" (a photo with a hyperlink to a detail page with special subject matter). The subject matter for each detail page is contained within a markdown file of the same name found within the detail-pages folder. These detail pages use the page template. The index.html contains permalinks corresponding to each detail page and the correct detail page markdown file is identified through the permalink indicated in the markdown file front matter. When the permalink is clicked on the homepage, the rendering engine identifies the markdown file associated with that permalink, fetches the page template and inserts the contents of the correct markdown file into the page template. 

Website style and image files are found in the css, images, and fonts folders.

### Primary Folder and File Structure

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
           children-and-youth-ministries.md
           church.md
           community-outreach.md
           global-church.md
           music-ministry.md
           pretty-prairie.md
           united-methodist-women.md
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

# High Level Folder and File Descriptions

| Folder/File                     | Description                                                           |
| ------------------------------- | --------------------------------------------------------------------- |
| README.md                       | Project info and instructions                                         |
| .gitignore                      | Instructs git of files to exclude when pushing files to git repo      |
| _config.yml                     | Website configurations                                                |
| _includes/                      | Partial templates to insert into _layouts folder files                |
| _layouts/                       | Templates that .html and .md file content is inserted into            |
| index.html                      | Website homepage                                                      |
| detail-pages/                   | Special subject content inserted into pages (linked to from Homepage) |
| posts/                          | Blog post content inserted into post template and Blog page           |
| about, activities, blog.html    | Main website pages which use the default layout template              |
| css/                            | Style files                                                           |
| images/                         | Image files                                                           |
| fonts/                          | Font files                                                            |

