# bootstrap-hexo-theme

A Hexo theme based around Bootstrap. Mobile-friendly and very customizable.

## Features
- Bootstrap UI themeable via your own ```bootstrap.css```
- Themable code-snippet highlighting via ```highlight.js```
- Comments - https://utteranc.es
- Google Analytics integration (just add your tracking_id)
- Google Custom Search Integration

## Install
1. Setup Hexo site
```
# Create hexo site
$ mkdir $working_directory$
$ cd $working_directory$
$ hexo init
$ npm install
# Install theme
$ git clone https://github.com/bendotbike/bootstrap-hexo-theme.git themes/bootstrap-hexo-theme
```
2. Remove ```themes/landscape```
3. Open ```_config.yml``` and change ```theme``` from ```landscape``` to ```bootstrap-hexo-theme```
4. Generate site ```hexo generate && hexo serve```
5. View your site at [localhost:4000](http://localhost:4000)

## Customize
### Foooter
Edit the content of ```layout/bootstrap-theme-hexo/partials/footer.ejs``` to add manually add custom content to your footer.
You can also add links to be displayed in the Footer section of ```bootstrap-theme-hexo/_config.yml```

## Pages

## Todo
- pagination
- figure out icon solution
- grunt script to minify CSS and JS, and to build site
- integrate google site search (search box in navbar?)
- finalize and polish download-page and project-page
