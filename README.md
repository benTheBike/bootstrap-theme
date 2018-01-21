
# bootstrap-theme 
A theme for Hexo based on Bootstrap. Allows for interchangeable Bootstrap themes. Features minimal dependencies and a clean design.

## Features
- Syntax highlighting w/ [Highlight.js](https://highlightjs.org/)
- Bootstrap UI with easily changeable ```bootstrap.min.css```
- Copy buttons for code blocks to copy code directly into user's clipboards
- ```project-page``` for displaying code projects
- ```download``` page for previewing file downloads

## How to use
### First, make sure you have Hexo installed (Instructions [here](https://hexo.io/docs/index.html#Installation))

### Now, create your Hexo site
*Note: ```hexo_site``` refers to the folder you create your Hexo site in ([Hexo docs](https://hexo.io/docs/setup.html))
```
$ mkdir C:/hexo_site
$ cd C:/hexo_site
$ hexo init
$ npm install
```


### Adding this theme to your site
```$ git clone https://github.com/benTheBike/bootstrap-theme.git C:/hexo_site/themes/bootstrap-theme```

Next, open up ```c:/hexo_site/_config.yml``` and change ```theme```'s value (which is ```landscape``` by default), to ```bootstrap-theme```.
### Now check it out
```
$ hexo generate
$ hexo serve
```
And your site should be located @ [http://localhost:4000](http://localhost:4000)

## Configure this theme
### _config.yml
This theme has it's own ```_config.yml``` located in ```themes/bootstrap-theme/_config.yml```. You can use it to modify:
- The Bootstrap theme in use. Leave it blank for the default. If you need a theme, I recommend [Bootswatch.com](https://bootswatch.com/)
- Theme color used in ```<meta name="theme-color">```
- Favicon
- Navbar items

### Other
CSS can be modified @ ```bootstrap-theme/source/css/styles.css```

Javascript can be added @ ```bootstrap-theme/source/js/main.js```

Add links to your own scripts/stylesheets @ ```bootstrap-theme/layout/partials/head.ejs``` and ```bootstrap-theme/layout/partials/scripts.ejs```.



## Site content
To add content of your site to this theme, take a look at these ```partials``` located in ```themes/bootstrap-theme/layout/partials```

- ```modal.ejs``` - the modal dialog displaying info about a post
- ```extra_post_info.ejs``` - info displayed after the main post info in the 'Post details' dialog box on a blog post
- ```head.ejs``` - add stylesheets here
- ```navbar.ejs``` - modify the navbar here
- ```scripts.ejs``` - add your own Javascript here

## Types of pages
### [post](https://hexo.io/docs/writing.html)
A regular Hexo post
```hexo new post-name```

### [page](https://hexo.io/docs/writing.html)
A regular Hexo page
```hexo new page page-name```

### download
A page for previewing a downloadable file
```hexo new page my-download-file``` 
Then navigate to ```C:/hexo_site/source/my-download-file/index.md```
In the [Frontmatter](https://hexo.io/docs/front-matter.html), modify the following
- layout - change to ```download```
- permalink - If you don't want the page at the site root, change this to something like ```downloads/my-download-file/index.html``` so the download link will look like ```example.com/downloads/my-download-file```
- filename - the name of the file (Ex. ```test.exe```)
- filetype - the type of the file. You can give a description for the user too (Ex. ```.exe (a Windows executable)```
- summary - a description of the file
- moreinfolink - a link to more information about the file being downloaded
- downloadlink - the link to the file download

And you can edit the content of the page to write a longer description/installation instructions/etc about the file.

### projectpage
A page for showing a project
```hexo new page my-project```
Then navigate to ```C:/hexo_site/source/my-project/index.md```
In the [Frontmatter](https://hexo.io/docs/front-matter.html), modify the following
- layout - change to ```projectpage```
- projectname - the name of the project
- permalink - If you don't want the page at the site root, change this to something like ```projects/my-project/index.html``` so the URL will look like ```example.com/projects/my-project```
- sourceurl - a link to the source code (like a Github link or something)
- downloadurl - A link to the download'
- subtitle - A short description

And you can edit the content of the page to write a longer description about the project.

## Other info
### Dependencies
This theme requires the following items to be located inside ```partials/head.ejs``` and ```partials/scripts.ejs``` (they are there by default, just don't remove them)
- Bootstrap & its dependencies
- Highlight.js

### To do
- Make highlight.js syntax highlighting theme an option in ```_config.yml```
- Run through ```hexo-unit-test``` and make necessary changes
- Add more detail to ```index.ejs```
