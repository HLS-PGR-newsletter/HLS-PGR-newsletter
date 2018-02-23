# HLS-PGR-newsletter.github.io
Coventry University's HLS postgraduate newsletter 

## How to add a new index of posts 

There are four steps included in making a new index to display a series of posts in chronological order.

1. Create a folder to contain the posts. This must start with an underscore, e.g. _reflections. This is where you will save all of the posts as .md files. 

2. Create an index page. This is a bit of html code that runs through all the posts placed in your folder you created in step one. You can use this index page as a reference from the [folder of articles](https://github.com/HLS-PGR-newsletter/HLS-PGR-newsletter.github.io/blob/master/article-index.html).
   
   There are three things you need to change if you copy and paste the raw code. The name of the file should be something informative such as reflections-index.html. The .html is important. Change the title and subtitle to whatever you want to show people when they open the page. 
   
   Finally, on line 9 there is this piece of code: 
   `{% for post in site.articles %}` You need to replace `articles` with whatever you want your collection to be called (more on that in step 3 but it makes sense to call it the same thing as your folder). 
   
3. In _config.yml, there is a section of code starting with `collections:`. You need to add another section with the name you used in step 2 (e.g. for `site.reflections` you would use `reflections:` under `collections:` (pay attention to the indents).
   
   Copy and paste the `ouput:` and `permalink:` lines. However you need to change the beginning of the permalink line to the name of your folder you specified in step 1, e.g. `permalink:   /_reflections/` and keep the remainder of the line the same. 

4. While you are still in _config.yml, the last thing you need to change is to specify where you want this page to be viewed in the navigation bar. Add the name of the index file you created in step 2 to the section starting with `navbar-links:`. To create an option in the header, simply specify what you want the name to be and write the name of the index file, e.g. `Reflections: 'reflections-index'`.   
   
