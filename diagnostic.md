# Rails API Diagnostic

Place your responses inside the fenced code-blocks where indicated by comments.

What is the purpose of a backend?

```md
The backend lets us store/retrieve data elements of a web application.
```

Which layer in the MVC pattern is used by the controller to fetch data?

```md
The controller uses a model to fetch data.
```

Which layer in the MVC pattern communicates with the model?

```md
The controller communicates with the model.
```

Why don't we use views in our interpretation of the MVC pattern?

```md
A view is what the user sees. A view will generate HTML, CSS, XML, Javascript, JSON. I'm guessing that since we're writing the view ourselves, we don't include them in the MVC pattern.
```

What does C.R.U.D stand for?

```md
Create, Read, Update, Delete
```

In which part of the MVC pattern can we find C.R.U.D actions?

```md
We can find CRUD actions in the controllers.
```

List at least 5 standard rails actions that C.R.U.D requests correspond to?

```md
INDEX
SHOW
CREATE
UPDATE
DESTROY
NEW
EDIT
```

A user action fires a `GET` request for `/people/1`. Explain in detail each step
required for data to be returned to the client. (bullet points or ordered list)

```md
1. The client fires a `GET` AJAX request to select the object with ID 1.
2. The web server receives the request. It uses a route to find (or a dispatcher to create) the appropriate controller.
3. The controller parses the request and finds the right model to address the request. The controller tells the model what it needs to do.
4. The model talks to the database and performs the steps to execute the request. It hands the result of the request back to the controller.
5. The controller takes the message from the model and sends a response body to the server.
6. The server compiles this data into an HTTP response. Then, the server sends that response to the client.
7. If the request is successful, the client will receive the data for the object with ID 1.
```

What is the command to generate a new rails-api app?

```bash
rails new rails_app_name
```

What is the command to start an instance of a rails server?

```bash
bin/rails server
```

What are the commands to drop, create, migrate and seed a database from the command
line? (5 bullet points)

```bash
- bin/rake db:drop
- bin/rake db:create
- bin/rake db:migrate
- bin/rake db:seed
- bin/rake db:examples
```

What is the command to scaffold a pet with a name and age attributes (hint:
Also think of the data types for each attribute)?

```bash
bin/rails generate scaffold pet name:string age:integer
```
