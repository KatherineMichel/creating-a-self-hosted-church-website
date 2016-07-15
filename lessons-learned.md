# Lessons Learned

* Each personal GitHub account is entitled to a gh-pages website with a root URL of http://accountname.github.io. For example, my portfolio website is a Jekyll site hosted on gh-pages with the root URL of http://katherinemichel.github.io. This URL will prepend the URLs of any additional gh-pages repo that I create. For example, an additional gh-pages repo named example-website will have the URL: http://katherinemichel.github.io/example-website as the homepage, not http://example-website.github.io. Usually, this prepending happens automatically, but not in the case of Jekyll. My biggest lessons learned, which required some time spent researching, was that I would need to modify the _config.yml in order to build the full URL, which I did like this:

    baseurl: "/self-hosted-church-website-jekyll" # the subpath of your site, e.g. /blog
    url: "https://katherinemichel.github.io/self-hosted-church-website-jekyll" # the base hostname & protocol for your site

I would also need to indicate within the code that the baseurl would need to be prepended to links, as I did here for the index.html: 

    <a class="blog-nav-item" href="{{ "/" | prepend: site.baseurl }}">Home</a>

Otherwise, the link would open as http://katherinemichel.github.io/index.html, rather than https://katherinemichel.github.io/self-hosted-church-website-jekyll/index.html
