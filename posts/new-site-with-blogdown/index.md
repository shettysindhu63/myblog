<!-- 
.. title: New site with blogdown
.. slug: new-site-with-blogdown
.. date: 2018-02-13 14:27:13 UTC+08:00
.. tags: R, communication
.. category: 
.. link: 
.. description: 
.. type: text
-->

*Disclaimer: This is not a tutorial, just notes on what steps I followed. For a comprehensive explanation, read the book [blogdown: Creating Websites with R Markdown](https://bookdown.org/yihui/blogdown/).*

<br>
This is a writeup on steps I took to setup a [personal website](https://sindhu.netlify.com/) with [blogdown](https://github.com/rstudio/blogdown) + [Hugo](https://gohugo.io/) + [Github](https://github.com/) + [Netlify](https://www.netlify.com/). I use [RStudio](https://www.rstudio.com/) to write the posts and project summaries in R Markdown. Since most of my projects are in R, I thought it would be good idea to setup a site for my project portfolio as well as more polished blog posts on use-cases for R packages and tutorials. Thanks to the [book](https://bookdown.org/yihui/blogdown/) on blogdown by the package author Yihui Xie, the process was quite smooth excluding the part where I took a whole day in selecting the theme (this was due to my indecisiveness). 

<!-- TEASER_END -->

<br>
#### Blogdown and Hugo 

- In R, type `install.packages('blogdown')` to install blogdown. 
- Create a new R project in an **empty directory** 
- Select a theme from [Hugo Themes](https://themes.gohugo.io/) and note down the GitHub repo. You will find this when you select Download on the theme homepage. Take note that not all themes are tested with blogdown. 
- In R, type `blogdown::new_site(theme = "theme_name")` where theme_name is the theme's GitHub repo `username/repo_name`. This will automatically create the required `config.toml` file. For default theme, use `blogdown::new_site()`
- Edit the `config.toml` file to your needs and change the structure in `content` directory as required. 
- Use RStudio Addin *New Post* to start writing new post and blogdown's LiveReload will show you preview of the website in RStudio viewer or web browser. If not, you can run `blogdown::serve_site()` or Addin *Serve Site*.

<br>
#### GitHub and Netlify

- Initialise git in your R Project folder and add `.gitignore` file with following: 
`.Rhistory`
`.Rproj.user`
`.RData`
`.Ruserdata`
Create a new remote repository in GitHub and push the local project folder to this remote repo. 
- In Netlify, you just need to connect the GitHub repository to your account and Netlify will deploy the site. Set **Build command** to hugo and **Publish directory** to public. Add new variable **HUGO_VERSION** and set it to the latest version of Hugo (which as of now is 0.36). You could just change the website name in the Netlify domain or change to a custom domain name. 

When you need to update the website, you just need to push the changes to the GitHub repo and Netlify will automatically reload the site with the changes. The time-consuming part would be tweaking the theme to your needs, so make sure to note all the changes you make to save time in future.