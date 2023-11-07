### Conceptual Exercise

Answer the following questions below:

- What are important differences between Python and JavaScript?

Python and Javascript have differents syntax. Talking about equality, when we compare an array like [1,2,3] == [1,2,3], in Python that comparison is strict about content, when in Javascript would be comparing the identity of the data. Python has a built-in test method which is the doctestes. In general Python throw more errors than JS, thats because some cases where JS would simply return an undefined value, python can crash all the code with a simple error.

- Given a dictionary like ``{"a": 1, "b": 2}``: , list two ways you
  can try to get a missing key (like "c") *without* your programming
  crashing.

  The best way would be with the built-in method for dictionaries "get". 'dict.get('data')
  Or you can do it using "try" and "catch"

- What is a unit test?
A unit test is a way of testing one portion of the code isolated from the application itself. Testing only one function from the program, for example.

- What is an integration test?
An integration test, unline unit test, is testing how all the parts of the code works together and how it interacts to each other.

- What is the role of web application framework, like Flask?
It's a set of code, functions, etc that helps to build more complex application and programs, not having to hardcode some parts.


- You can pass information to Flask either as a parameter in a route URL
  (like '/foods/pretzel') or using a URL query param (like
  'foods?type=pretzel'). How might you choose which one is a better fit
  for an application?
A URL parameter feels like more the subject of the page. While the Query Parameters is related to extra info about a page. Usually used when coming from a form.

- How do you collect data from a URL placeholder parameter using Flask?

You define a variable in the app.route url parameter and then uses that same variable as parameter for the routing function.

```py
@app.route('/url/<param>')
def search(param)
```

- How do you collect data from the query string using Flask?

You request using request.args.get("data") where data would be the name of the input you are trying to retrieve the info.

- How do you collect data from the body of the request using Flask?

Using the request.form.get("data"). 

- What is a cookie and what kinds of things are they commonly used for?
A cookie is piece of information which stores the domain, "key", and "value" that gets sent from the server to the client. It allows the client to send back that information to the server so the server can use that information. It allows for a user to go back in to a session to resume where they left off.

- What is the session object in Flask?
The session object is built off of using cookies. It allows the server to set many different things in the session for the client to remember without having to create many different cookies and just have one session. It is also encoded so that someone can't change session data on the client before sending it to the server.


- What does Flask's `jsonify()` do?

Will convert a JSON serializeable data in python to a JSON string.
