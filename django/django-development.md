# Django- Development

Django version of the self-hosted [church website](https://self-hosted-church-website.herokuapp.com) and [code](https://github.com/KatherineMichel/self-hosted-church-website-django)<br>

## Code Explainer

I have used the [Heroku Django Template](https://github.com/heroku/heroku-django-template), which is deployment ready. The template can be deployed for free via [Heroku free tier](https://www.heroku.com/pricing). One change I have made for deployment, is to add python-decouple to the requirements.txt before installation, update the settings.py and move the SECRET_KEY to the .env file, which is included in the .gitignore so it will not be committed to source control. The SECRET_KEY is sensitive information and should not be made public in production. 

Most pages are static and are rendered from self_hosted_church_website_django/urls.py as a TemplateView and the domain name will prepend the URL. The Blog pages are the exception. A special app called "blog" has been created. An entry in self_hosted_church_website_django/urls.py points to blog/urls.py, which contains the Blog URLs. Because these URLs are at the app level, the Blog URL will be www.domain-name/blog and the post pages will be prepended with www.domain-name/blog. blog/models.py contains a blog post model and blog/views.py contains a view for the Blog page and post pages. The Blog page template contains a for loop that will fetch each post and insert the post info into the template. This loop will continue until every post is displayed, to form a list. The post-detail template does not need a for loop because only one post will be displayed, with the applicable info again inserted into the template. 

The project-level settings have been altered to look for static files and templates outside of the app folder. Therefore, all static files and templates are in root folders. Soft-coded links to individual static files can found in the templates. URL hyperlinks are based on the "name" variable in self_hosted_church_website_django/urls.py and blog/urls.py.

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
| manage.py                                       |                                                                       |
| Procfile                                        | Heroku deployment config file (stands for process file)               |
| requirements.txt                                | Heroku deployment config file                                         |
| runtime.txt                                     | Heroku deployment config file                                         |
| self_hosted_church_website_django/_init_.py     |                                                                       |
| self_hosted_church_website_django/settings.py   | Project-level settings                                                |
| self_hosted_church_website_django/urls.py       | Project-level urls                                                    |
| self_hosted_church_website_django/wsgi.py       |                                                                       |
| db.sqlite3                                      | Local database file. Could be included in .gitignore                  |
| blog/_init_.py                                  |                                                                       | | blog/admin.py                                   |                                                                       | | blog/apps.py                                    |                                                                       | | blog/models.py                                  | App-level models                                                      | | blog/tests.py                                   |                                                                       |  | blog/urls.py                                    | App-level urls                                                        | | blog/views.py                                   | App-level views                                                       |
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
