# Mission-to-Mars
Web scraping methods to extract data using Chrome Developer tools to identify HTML components, Beautiful Soup/Splinter to automate the scrape, MongoDB to store the data, and Flask to display the data.

## Main Objectives
1. Use HTML elements, as well as class and id attributes, to identify content for web scraping.
2. Use BeautifulSoup and Splinter to automate a web browser and perform a web scrape.
3. Create a MongoDB database to store data from the web scrape.
4. Create a web application with Flask to display the data from the web scrape.
5. Create an HTML/CSS portfolio to showcase projects.
6. Use Bootstrap components to polish and customize the portfolio.

The goal was to develop an app to scrape the following information about the planet Mars:

* Latest News
* Featured Image
* Facts about the planet
* Images of the hemispheres

### Deliverable 1
Create ["Mission_to_Mars_Challenge.ipynb"](https://github.com/tiffanylin706/Mission-to-Mars/blob/9ad4d6f71f2e1e67b9cebcffb97bc35b011051f5/Mission_to_Mars_Challenge.ipynb jupyter notebook) in `Jupyter notebook` to perform the scraping activity and pull the requested information needed to build the app. 
For Example:
* Visiting the URL `url = 'https://redplanetscience.com/', browser.visit(url)`
* Using `Splinter` and `BeautifulSoup` to automate the browser and parse the HTML element to obtain the latest news title `news_soup = soup(html,'html.parser')`, `slide_elem.find("div",class_='content_title')`, `news_title = slide_elem.find("div", class_='content_title').get_text()`

 ![D1 jupyter notebook](https://github.com/tiffanylin706/Mission-to-Mars/blob/8b67554cee2d70dce3320aa249998adcceb730de/Resources/D1-jupyternotebook.png)

### Deliverable 2: Update the Web App with Mars’s Hemisphere Images and Titles
Next, we exported our `Jupyter notebook` file into a `Python` [script](https://github.com/tiffanylin706/Mission-to-Mars/blob/9ad4d6f71f2e1e67b9cebcffb97bc35b011051f5/Mission_to_Mars_Challenge.py). Using this script as the starting point, we started to define the scraping process using `Visual Studio Code` to edit our `Python` script. We added functions to scrape through the website(s) and loop through the HTML tags to return the information used to create a database to be stored in `MongoDB`.

 ![D2 define](https://github.com/tiffanylin706/Mission-to-Mars/blob/55f382b7628e263a14742d951dd1a489d3de8a51/Resources/D2-%20define.png%20.png)

Using the database in `Mongo`, we create a `Flask` app to connect to the information and create our app routes. These [routes](https://github.com/tiffanylin706/Mission-to-Mars/blob/9ad4d6f71f2e1e67b9cebcffb97bc35b011051f5/app.py) help to display the information on the home page and will perform the scraping of new data using the codes that we wrote in the `Python` script. 

Next, we integrate `Mongo` into the web app so that the data stored is updated every time the script, ["Scraping.py"](https://github.com/tiffanylin706/Mission-to-Mars/blob/9ad4d6f71f2e1e67b9cebcffb97bc35b011051f5/scraping.py) is run.

After, we create an [HTML template](https://github.com/tiffanylin706/Mission-to-Mars/blob/9ad4d6f71f2e1e67b9cebcffb97bc35b011051f5/templates/index.html) to customize the the web app and use `Bootstrap` components to enhance the HTML and CSS the file.

Lastly, we modified the HTML file to loop through the dictionary and pull the titles and images for the hemispheres of Mars.
 ![D2-1 hemisphere](https://github.com/tiffanylin706/Mission-to-Mars/blob/55f382b7628e263a14742d951dd1a489d3de8a51/Resources/D2-1%20%20hemisphere.png) 

### Deliverable 3: Using Bootstrap 3 to modify the html file
## The webpage is mobile-responsive
Changed everything to col-xs, which is the smallest option.  Everything will scale up from the mobile phones size to the larger desktop sizes. 

## Two additional Bootstrap 3 components are used to style the webpage
1. Changed the button color to warning, which is orange to match the header color.
2. Added a tooltip that says Click Me!, when the user hoovers over the Scrape button.
3. Bonus: Changed the colors of various areas, adjusted some heights, and added a striped table pattern.

![D3 Bootstrap](https://github.com/tiffanylin706/Mission-to-Mars/blob/55f382b7628e263a14742d951dd1a489d3de8a51/Resources/D3.png)
