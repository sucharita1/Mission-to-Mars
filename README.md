# Mission-to-Mars
Scrape all data on the web on mission to Mars and store it in MongoDB and finally put it together on a web application based on flask.

## Overview of the Analysis
A junior data scientist Robin does freelance astronomy work in her spare time. Her dream is to land a position with NASA someday. So she spends a lot of time visiting sites with news about space exploration, especially the mission to Mars. She plans to build a web application that will scrape new data from web every time she tells it to at the click of a button. We help her write the python script that can navigate the webpages to collect the information. Once we have all the data we will use a NoSQL database MongoDB, as we'll be downloading tables for sure but also paragraphs and images. Now, to put it all together on a web application of we will use Flask, a web framework that allows us to create a web application using python and then customise it with HTML and CSS. 

## Resources
Software: Python-3.7.10, Jupyter notebook 6.3.0,splinter-0.17.0, bs4, webdriver-manager chrome,flask-1.1.2, Bootstrap-3
Database:  Mongodb- v5.0.3

## Results
#### Scraping the Full-Resolution Mars Hemisphere Images and Titles
* [Mission_to_Mars_Challenge.ipynb](https://github.com/sucharita1/Mission-to-Mars/blob/c2df349a4e62814988b42af6fcd929d98a00bb1c/Mission_to_Mars_Challenge.ipynb) that clicks on each hemispheric link and retrieves ALL full-resolution images and titles of the four hemisphere images. 
* ALL full-resolution images are added to the dictionary, hemispheres.
* The dictionary that contains full-resolution image URLs and image titles is added to a list, hemisphere_image_urls.
![hemisphere_image_urls](https://github.com/sucharita1/Mission-to-Mars/blob/c2df349a4e62814988b42af6fcd929d98a00bb1c/Resources/hemisphere_image_urls.png?raw=true)

#### Updating the Web App with Mars Hemisphere Images
* The [scraping.py](https://github.com/sucharita1/Mission-to-Mars/blob/c2df349a4e62814988b42af6fcd929d98a00bb1c/scraping.py) file is updated and retrieves ALL FOUR of the full-resolution image URLs and titles. 
* The mongo database is updated to contain ALL FOUR of the full-resolution image URLs and titles. 
![mongodb_mars_db](https://github.com/sucharita1/Mission-to-Mars/blob/c2df349a4e62814988b42af6fcd929d98a00bb1c/Resources/mongodb_mars_db.png?raw=true)
* The [index.html](https://github.com/sucharita1/Mission-to-Mars/blob/c2df349a4e62814988b42af6fcd929d98a00bb1c/templates/index.html) file contains code that will display the full-resolution image URLs and titles.
* The [app.py](https://github.com/sucharita1/Mission-to-Mars/blob/c2df349a4e62814988b42af6fcd929d98a00bb1c/app.py) contains flask scripts that link all the information from this module and ALL FOUR full-resolution images and titles of the four hemisphere images to a webpage.

#### Add Bootstrap 3 Components
* The webpage is mobile responsive and can be viewed in a laptop, mobile or an ipad.
![responsive_url](https://github.com/sucharita1/Mission-to-Mars/blob/c2df349a4e62814988b42af6fcd929d98a00bb1c/Resources/responsive_url.png?raw=true)
* TWO additional Bootstrap 3 components are used to style the webpage are :
1. The Scrape New Data Button is converted to btn-primary to btn-warning to match the colour of Red planet Mars. The background colour of jumbotron heading is changed to DarkSalmon to match the Red planet Mars.
![styles_button_heading](https://github.com/sucharita1/Mission-to-Mars/blob/c2df349a4e62814988b42af6fcd929d98a00bb1c/Resources/styles_button_heading.png?raw=true)
2. Mars Facts Table is given border with DarkSalmon background to match the whole website ode to Mars and the data is centred to give the table a better look.

![styles_table_border_heading](https://github.com/sucharita1/Mission-to-Mars/blob/c2df349a4e62814988b42af6fcd929d98a00bb1c/Resources/styles_table_border_heading.png?raw=true)
