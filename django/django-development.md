# Django- Development

Django version of the self-hosted [church website](https://self-hosted-church-website.herokuapp.com) and [code](https://github.com/KatherineMichel/self-hosted-church-website-django)<br>

## Code Explainer

I have used the [Heroku Django Template](https://github.com/heroku/heroku-django-template), which is deployment ready. The template can be deployed for free via [Heroku free tier](https://www.heroku.com/pricing). I followed the Heroku Django Template instructions, including creating a virtual environment for the project. 

However, I did make one change before pushing my new project to my own GitHub repo. I added python-decouple to the requirements.txt before installation, updated the settings.py, and moved the SECRET_KEY to the .env file. A SECRET_KEY used in production is sensitive information and should not be committed to public source control. I then included the .env file in the .gitignore, so that the .env would remain local and not be pushed to my public GitHub repo. By the way, I used a [GitHub Python .gitignore template](https://github.com/github/gitignore).

All static files are stored in a root folder called static. All templates are stored in a root folder called templates. The project-level self_hosted_church_website_django/settings.py has been altered so that the static files and templates are located in these root folders, rather than in an app folder. All templates extend from base.html template, which includes soft-coded links to the CSS files. Other templates contain soft-coded links to other static files such as images as needed.

Most of the website pages are static and are rendered at a project-level from self_hosted_church_website_django/urls.py as TemplateView. This means that the templates are fetched from the templates folder based on name and rendered without any need for a model or view. The domain name will prepend the URL I have specified for each of these pages in self_hosted_church_website_django/urls.py. 

The Blog requires a model, so these pages cannot be rendered as a simple TemplateView. I have created an app called "blog." In the blog folder are a models.py file containing the blog model and a views.py file containing views for the Blog page and the post detail pages. An entry in the project-level self_hosted_church_website_django/urls.py points to the app-level blog/urls.py, which contains the Blog page and post detail URLs. Because the URLs in the blog/urls.py are app-level, the Blog page URL will be www.domain-name/blog, and the post detail pages will be prepended with www.domain-name/blog. pk model variable and a regular expression in blog/urls.py make it possible for post detail pages to be rendered when blog posts are created in the future. 

The Blog page template contains a for loop that will fetch each post and insert the post info into the template. This loop will continue until every post is displayed, to form a list. The post-detail template does not need a for loop because only one post will be displayed, with the applicable info again inserted into the template. 

URL hyperlinks are based on the "name" variable in self_hosted_church_website_django/urls.py and blog/urls.py.

<!--
Admin: The blog model fields map to information inputted. 
-->

## Primary Folder and File Structure

    .env
    .gitignore
    manage.py
    Procfile
    README.md
    requirements.txt
    runtime.txt
    self_hosted_church_website_django/
           _init_.py
           settings.py
           urls.py
           wsgi.py
    db.sqlite3
    blog/
           _init_.py
           admin.py
           apps.py
           models.py
           tests.py
           urls.py
           views.py
    static/    
           css/
                bootstrap.css
                bootstrap.min.css
                main.css
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
    templates/
           404.html
           about.html
           activities.html
           base.html
           blog.html
           home.html             
           post-detail.html             
           detail-pages/
                children-and-youth-ministries.html
                church.html
                community-outreach.html
                global-church.html
                music-ministry.html
                pretty-prairie.html
                united-methodist-women.html
                welcome.html
                worship.html
           
## High Level Folder and File Descriptions

| Folder/File                                     | Description                                                           |
| ----------------------------------------------- | --------------------------------------------------------------------- |
| README.md                                       | Project info and instructions                                         |
| .env                                            | Contains sensitive env variables and is included in .gitignore        |
| .gitignore                                      | Instructs git of files to exclude when pushing files to git repo      |
| manage.py                                       | Django config file                                                    |
| Procfile                                        | Heroku deployment config file (stands for process file)               |
| requirements.txt                                | Django dependencies file for automated installation                   |
| runtime.txt                                     | Heroku deployment config file                                         |
| self_hosted_church_website_django/_init_.py     |                                                                       |
| self_hosted_church_website_django/settings.py   | Project-level settings                                                |
| self_hosted_church_website_django/urls.py       | Project-level urls                                                    |
| self_hosted_church_website_django/wsgi.py       |                                                                       |
| db.sqlite3                                      | Local database file. Could be included in .gitignore                  |
| blog/_init_.py                                  |                                                                       | 
| blog/admin.py                                   | App-level admin                                                       | 
| blog/apps.py                                    |                                                                       | 
| blog/models.py                                  | App-level models                                                      | 
| blog/tests.py                                   |                                                                       | 
| blog/urls.py                                    | App-level urls                                                        | 
| blog/views.py                                   | App-level views                                                       |
| static/css/                                     | Style files                                                           |
| static/images/                                  | Image files                                                           |
| static/fonts/                                   | Font files                                                            |
| templates/404.html                              | Page not found template                                               |
| templates/about.html                            | About page template                                                   |
| templates/activities.html                       | Activities page template                                              |
| templates/base.html                             | All other templates extend from this template                         |
| templates/blog.html                             | Blog template                                                         |
| templates/home.html                             | Website homepage template                                             |
| templates/post-detail.html                      | Blog post detail template                                             |
| templates/detail-pages/                         | Templates for detail-pages linked to from Homepage                    |
