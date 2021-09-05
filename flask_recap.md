# Flask Recap

This week we've built out the back end of an app and added data persistence in the form of PostgreSQL. This week we've been building the `M` in MVC.

![MVC](img/mvc.png)

Our next step will be to add Flask. Flask will provide us with the `V` and the `C`.

Let's review what Flask is and where it will fit in our applications.

Flask is a web framework for building web applications with Python. 

## Task

Your task is to review the Events App that we built last week. Ask yourself the following questions:

1. What does the directory structure look like? 
EVENTS
  controllers
      controller.py
  models
      event_list.py
      event.py    
  static
      style.css
  templates
      base.html
      index.html
  .flaskenv
  app.py

2. What are the different parts that make up the app?

Models
Controllers
View 

3. What are controllers responsible for?

Controllers are responsible for returning a response when a user makes a request in the browser. 

4. What are templates responsible for?

Templates allow us to structure content for users using HTML.

5. What is the static folder for?

The Static folder contains content that will always be the same each time the user views it.  CSS files are stored in the Static folder.

5. How do you think we will combine what we've done this week with Flask?

Now we can create a database, we can bring everything together to build a webpage where data can be added to by the user.  The difference being now that each time we quit and run flask the data will still be there. 

6. How do you create a `route` in the controller?

@app.route('/')  function or method

@app.route('/events')
def index():
    return render_template('index.html', title='Home', events=events)

When the URL is put into the browser the function is called and the user will see the output on the screen.
 
7. The `models/events.py` file acted as some dummy data for our app. This will no longer be necessary. Why is that the case?

This dummy data file will no longer be needed as we can now create a database, the user will be able to enter the content straight onto the webpage.


