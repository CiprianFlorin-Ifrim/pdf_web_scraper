# Python Selenium PDF Web Scraper
This Python script utilizes Selenium to automate the process of downloading PDF files from a specified webpage. It's designed for those who need to automate the retrieval of PDF documents from web pages for analysis, archiving, or any other purpose.

### 1. Features
- Automated download of PDF files from a specified URL.
- Customizable to target specific PDF links or documents.
- Utilizes Selenium WebDriver for robust interaction with web elements.

### 2. Requirements
- Python 3.6 or higher
- Selenium WebDriver
- Appropriate WebDriver for the browser you intend to use (e.g., ChromeDriver for Google Chrome)

### 3. Usage
- First, ensure you have Python installed on your system. Then, install the required packages using pip.
- Clone this repository or the notebook to your local machine.
- Edit the notebook to specify the target webpage and any necessary login or navigation steps to access the PDF files.
- Run the script from Jupyter Notebook or other IDEs.

### 4. Notes:
- There is one notebook called "esc_report_scraper_skipcaptcha" which gets the PDF links directly from the download button element, skipping all forms and captchas. This happens because the website is made to ask for captcha only the first time the user downloads a file, and then uses cookies to store the data, resulting in the download link being always available either directly attached in the HREF of the button or in a hidden form available with a different CSS selector element.
- There is also an experimental script that can complete forms and captchas. It will automatically input set user text in text boxes, randomly choose items from dropdown menus and tick captcha checkboxes, while also submitting the form to proceed with the page. Please note that certain pages have a multi-form setup, where one form is shown for 1 download, and another more complex form is shown after that. This could also be due to the fingerprint of the Browser instance running through Selenium. Due to this, although this notebook can input and complete multiple forms, it is not fully finished due to the high time requirement to have a proper try-catch tree structure for the multitude of elements needed.
- Sometimes, after multiple instances of the Selenium browser running, the captcha will change from a tick checkbox to a problem to solve. In that case a separate implementation and library is needed, with something like [NopeCHA](hhttps://github.com/NopeCHALLC/nopecha-extension)

### 4. Youtube Demos:

#### Automatic PDF Reports Web Scraping with Selenium and Python

[![Web Form and Captcha Solver](http://img.youtube.com/vi/iDx3MOHf9BU/0.jpg)](http://www.youtube.com/watch?v=iDx3MOHf9BU)

#### Web Form and Captcha Solver 

[![Web Form and Captcha Solver](http://img.youtube.com/vi/pm18ry0rxjo/0.jpg)](http://www.youtube.com/watch?v=pm18ry0rxjo)

### 4. Other personal examples of Web Scraping:

#### Rapid Chart Scraping from Coindesk with Python and Selenium

[![Rapid Chart Scraping from Coindesk with Python and Selenium](http://img.youtube.com/vi/WjXMw7vbC3M/0.jpg)](https://youtu.be/WjXMw7vbC3M?si=ONbciHWYeQGSyYJ2)


#### Automated Plot Scraping from Trading Websites with Selenium

[![Automated Plot Scraping from Trading Websites with Selenium](http://img.youtube.com/vi/9yvP1M8YaDo/0.jpg)](https://youtu.be/9yvP1M8YaDo?si=G4pQ7zEWUl7wQMO7)
