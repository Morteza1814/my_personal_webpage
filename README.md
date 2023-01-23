## My personal homepage template

This is a template of my [personal website](https://www.cs.virginia.edu/~rgq5aw/). It is a static website and the HTML code is generated by pug (see here for a guide on [pugjs]([pug](https://pugjs.org/api/getting-started.html)) syntax.

### Prerequisites 

Install the following packages before running the build scripts.
```bash
apt-get install npm
npm install pug-cli -g
apt install node-less
npm install -g less
npm install -g less-plugin-clean-css
```

### How to use this template

Everything that needs to be changed is in ```html/params```:

- *aboutme.pug*: contains the text which goes to **About me** section of the website.
- *news.pug*: contains the news that apear in the **homepage** and **news** section of the website. ```newsHighlights``` variable in *news.pug* determines the number of news to be show in **homepage**.
- *papers.pug*: contains the papers section of the website
- *posts.pug*: contains the summary of posts (title, publish date, and a short summary) that apear in the **homepage** and **blog** section of the website. ```blogPostHighlights``` variable in *news.pug* determines the number of news to be show in **homepage**.
- *projects.pug*: contains the project section of the website
- *reviews.pug*: contains the **Professional Activities** section of the **homepage**.

Then you need to compile the *pug* code and obtain the html code of the website. To do so, use ```build.sh``` script. The script simply compiles the pugjs code and generated the corresponding HTML/CSS of the website, and puts them in ```build``` directory. 

### How to deploy your website using this template
Simply move the generate HTML/CSS codes by ```build.sh``` script from ```build``` directory to ```public_html``` directory of the server hosting your website.
** Use [this](https://stackoverflow.com/questions/18088372/how-to-npm-install-global-not-as-root) to help installing the required packages. 
