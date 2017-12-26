# bootstrap-theme (Still in development)
A theme for Hexo based on Bootstrap. Allows for interchangable Bootstrap themes. Features minimal dependencies and a clean design.

## Features
- Syntax highlighting w/ [Highlight.js](https://highlightjs.org/)
- Bootstrap UI with easily changable ```bootstrap.min.css```
- Copy buttons for code blocks to copy code directly into user's clipboards

## How to use
### Create your site
```
mkdir c:/MySite
cd MySite
hexo init
npm install
```
([Hexo docs](https://hexo.io/docs/setup.html))

### Adding this theme to your site
```git clone https://github.com/benTheBike/bootstrap-theme.git c:/MySite/themes```

Next, open up ```c:/MySite/_config.yml``` and change ```theme```'s value (which is "landscape" by default), to ```bootstrap-theme```.
### Now check it out
```
hexo generate
hexo serve
```
And your site should be located @ ```http://localhost:4000```

## Configure this theme
### _config.yml
This theme has it's own ```_config.yml``` located in ```themes/bootstrap-theme/_config.yml```. You can use it to modify:
- The Bootstrap theme in use. Leave it blank for the default. If you need a theme, I reccomend [Bootswatch.com](https://bootswatch.com/)
- Theme color used in ```<meta name="theme-color">```
- Favicon
- Navbar items

### Other
You can also style any other part of the site by modifying the stylesheet located at: ```themes/bootstrap-theme/source/css/styles.css```. And add your own javascript in ```themes/bootstrap-theme/source/js/main.js```

## Site content
To add content of your site to this theme, take a look at these ```partials``` located in ```themes/bootstrap-theme/layout/partials```
- ```extra_post_info.ejs``` - info displayed after the main post info in the 'Post details' dialog box on a blog post
- ```head.ejs``` - add stylesheets here
- ```navbar.ejs``` - modify the navbar here
- ```scripts.ejs``` - add your own Javascript here

## Other info
### Dependancies
This theme requires the following items to be located inside ```partials/head.ejs``` and ```partials/scripts.ejs``` (they are there by default, just don't remove them)
- Bootstrap & its dependancies
- Highlight.js

### To do
- Add other pages, such as download & code-project
- Make highlight.js syntax highlighting theme an option in ```_config.yml```
- Run throught ```hexo-unit-test``` and make necessary changes
- Add more detail to ```index.ejs```
