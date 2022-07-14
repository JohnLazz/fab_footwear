<h1>Code Institute Milestone 4 Project.</h1>

<h3>Fab Footwear e-commerce store selling mens footwear.</h3>
<hr>

**This project is incomplete due to external circumstances and work so far is a customised version of the code-along project 'Boutique Ado'. Below are the notes I had so far during development.**

<hr>

superuser credentials: user = "admin1", pword = "admin1"

TECHNOLOGIES USED: 
html, ccs
bootstrap 4.6 
django
django allauth
other dependancies in requirements.txt

OTHER TOOLS:
Online JSON formatter 'https://elmah.io/tools/json-formatter/' used to check self made fixtures.

Attributions: 
Base, index and nav with css initially taken from Boutique Ado project from Code Institute and later customised (planned to further customise) by me.

Hero Photo by Nicholas Kampouris on https://unsplash.com/photos/ZIW_wcbjKLw
Shoe images from 'https://www.kaggle.com/datasets/noobyogi0100/shoe-dataset'.

_____________________________________________________________________________
TESTING

ALLAUTH: Using the path extention /accounts/login and logging in using superuser credentials takes us to /confirm-email/ therefor allauth is working
as confirming email is working. 
Updating email as verified in the django admin settings we can set the path of LOGIN_REDIRECT_URL = '/success' which confirms authentication and log in 
settings are all working. (/success does not exist but shows up in browser url when logging in). This can be changed back to '/' to redirect to 
home page after a user logs in.

FIXTURES: Make sure all categories and product fixtures have loaded correctly by viewing them in django /admin.
Hadn't added .jpeg to 23/24 of the products in the products.json fixture so had to delete all the products in the admin panel, ammend the fixtures and use loaddata products
again to update the database.

IMAGES: https://stackoverflow.com/questions/37287153/how-to-get-images-in-bootstraps-card-to-be-the-same-height-width
above link uses css to keep images in card from interferring with the rest of the card, changed object-fit: cover; to object-fit: scale-down;

Ammended if forloop.counter to display hr after 'x' cols to display 1,2 or 3 cards instead of up to 4 and made hr visibility:hidden so it's only used for spacing.

Search Queries: Not all products have the footwear type within the name or description (example 'The Rustic Cowboy' doesn't have 'boot' in name or desc)
therefore users would have to use the categories drop down to filter all 'boots' instead of searching 'boots'.

