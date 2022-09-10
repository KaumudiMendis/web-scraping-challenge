# Monash Data Course Wk 12 Assignment
## web-scraping-challenge

## Part 1 - Python/Jupyter Scraping

Using the provided URLs from the assignment doc, browser opened and required data pulled.

The news_title and news_p variables from https://redplanetscience.com/.
    Site scraped with BeautifulSoup. 
    The title found in the html with the element "div" class "content_title".
    The paragraph found under "article_teaser_body". 
    Pulled the actual text out from the element using Both .find() functions 
    followed with the .get_text().

The featured image - 
    Used splinter from https://spaceimages-mars.com/. 
    Clicked on the "FULL SIZE" button. 
    Utilised the .find_by_partial_text() and .click() functions.
    The source of the image was pulled using BeautifulSoup .find() function.
    Used square brackets to call and where the image source was found within the class "fancybox-image"  
    The "src" was pulled by using square brackets to call.

The table data called using pandas scraping. 
    Utilised the .read_html() function on the url https://galaxyfacts-mars.com/.
    Print out the table to find the correct data. 
    The 0th table is pulled for the Mars facts, renamed the columns from 0,1,2 to description,Mars,Earth, using the .rename() function. 
    The index is set to the Description column to finish off the formatting of the table. 
    Stored the data as a varibale in html using the .to_html() function.

Access the url https://marshemispheres.com/ and use splinter to scrape the full sized hemisphere images. 
    Repeated the same actions for each image using a for loop. 
    Access the thumbnail link using .find_by_css() and .click(). 
    Stored the title and image source into a dictionary.
    Appended the dictionary to an existing list to have one variable to hold all the information for all 4 images.


## Part 2 - Flask/MongoDB/HTML
Jupyter file was placed within a python file - scrape_mars, and accessed by app.py file. 
The results written to a dictionary containing each data item separately to make to call within the html.

The app.py file is the Flask basis for index.html which utilises a connection to MongoDB which allows to scraped data.

The html file was created and the result web image provided.
