# Amazon-Price-Tracker
A simple python web scraper which scrapes the price of the desired item from the Amazon and check against the user wanted price. If it satisfied the user price then it will send the mail to the user. 

## Libraries used :
  
  
### Requests Library
  The requests module allows you to send HTTP requests using Python.
  
### BeautifulSoup
  Beautiful Soup is a Python library that is used for web scraping purposes to pull the data out of HTML and XML files. It creates a parse tree from page source code that can be used to extract data in a hierarchical and more readable manner.

### SMTPLIB
  Simple Mail Transfer Protocol (SMTP) is a protocol, which handles sending e-mail and routing e-mail between mail servers.

  Python provides smtplib module, which defines an SMTP client session object that can be used to send mail to any Internet machine with an SMTP or ESMTP listener daemon.
  
--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

 ### URL
  Store the URL of the desired product in the URL variable in the source code.
  
 ### UserAgent 
  Get the user-agent of your browser by just typing my user agent in the google. It will give a long long string just copy it. 
  
  Then create a dictionary names headers. The key is User-Agent and the value is which we copied earlier.
  
 ### Checking Price ()
 
 First things first after defining everything we need in the project let's get into action. 
 
 Define a function for scraping and checking the price of the product.
 
 To get the contents of the page we make use of the requests library's get function. We pass the User-Agent and URL as arguments and store the result in the page variable.
 
 After scraping we pass the page variable to the soup function and parse the HTML.
 
 So now our data is contained and formatted. Now we need to find the price inside the HTML. Just go and inspect the browser in the product page and find the price's id.
 
 Now we got our price but it's yet to be processed since it can not be used to compare or perform any manipulations.
 
 Initially we remove the currency symbol .
 
 Also we remove the commas from the price.
 
 Then we set the user desired price. If the price of the product falls below the user given price then it will call the send_mail() function.
 
 Just bare with me we almost done dude.!
 
 ### Send Mail ()
 
 First we need to establish the connection with the GMail's server. So we set up a server. (Refer the code)
 
 Once we established the connection we need to trigger the connection using the ehlo function.
 
 Our connection must be an encrypted one so we use startts function
 
 A two factor authentication password has to be set up for your mail. Once it set up you will be provided a password for using in certain environments alone. 
 
 Then we need to log in to the server . The first argument is our mail id and the second argument is two factor authentication password.
 
 Afterwards we defin the subject and body of the mail.
 
 Then once we done we use the sendmail function to send the mail to the user account. It has two arguments one is the server mail and another is user's mail.
 
 Then we quit the server connection.
 
TADAAAAAAAAAA We are done. Happy Coding :)

It may not be a good documentation but I believe that it satisfy basics. 
 
 

