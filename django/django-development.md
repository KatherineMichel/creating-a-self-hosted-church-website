# Django- Development

Django version of the self-hosted [church website](https://self-hosted-church-website.herokuapp.com) and [code](https://github.com/KatherineMichel/self-hosted-church-website-django)<br>

## Code Explainer

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
                children-and-youth-ministries.md
                church.md
                community-outreach.md
                global-church.md
                music-ministry.md
                pretty-prairie.md
                united-methodist-women.md
                welcome.md
                worship.md
           
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
| templates/detail-pages/                         |                                                                       |


| detail-pages/                                   | Special subject content inserted into pages (linked to from Hompage)  |
