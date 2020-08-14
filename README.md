Attempting to recreate an existing Shopify Store to get practice of Liquid Templating. 

The store I've chosen is: https://www.truefittandhill.ca/

The 2 elements I want to focus on re-creating are:
- Navigation Header
- Footer

For this first release I'm gonna skip past everything in the homepage.

The challenge currently in front of me is figuring out where the HTML and CSS styling elements go into and how do I get it on the browser. Step #1. 

Okay, got that sorted. Next up I want to get the top bar showing up - on the site it currently says "Free Shipping on Orders over $50" and has a icon as well. This is going to be interesting. 

In the Admin Panel I want to add a section that allows the admin to add an icon and the message. I'm not gonna use fonts at this point and the assumption is the text will print as is, no currency translations. 

Interesting. 

Let's break this down into doable chunks:
1 - Use a blog post to publish the content in the frontend. Call using blog slug. This is such a WordPress way of thinking lol. I'm gonna need a better way to do this next, but until then I hack away at it.
2 - Once that is done figure out how to create a custom type in the Shopify Admin Panel. 

Right so I have done #1 which is create a Blog post for the header content. This has the SEO-slug:
top-alert

How do I render this in the frontend? That's an interesting challenge, let's dive into Shopify Controllers / way of passing content to the frontend. 

I'm gonna need an App for this. Yay. More config stuff. 

This is interesting though, I could use AWS and host my services independently of the Shopify store itself. Your app is essentially a micro-service that serves the Shopify Store. It uses something called the Shopify App Bridge.

Enabled Blog Access to the Shopify App I created. This should now allow me the option to create a custom app (in Python? C? JS? PHP?) to read the Blog Post by tag name from Shopify. 

So, maybe need to use the GraphQL Query to retrieve data from the server - similar to a GET request for a REST API. 

Gonna switch tracks a bit because blogs are hard to capture. Let's move on and fetch a single product instead. Gonna create a Product in my Development Store now. 

Okay, gotta shift gears, turns out the home page auto displays 4 products a la code in index.liquid. Added one line custom html there just to test. Works fine. I have access to all the HTML and CSS on the Page. Haven't quiet figured out how to fetch individual content yet, that's still to be figured out. I know I can do it using GraphQL and Python, just got to write the script and host it up somewhere. 

