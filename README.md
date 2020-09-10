# About
A simple todo app, that uses REST to work with a todo list.
The data will be persisted in a virtual database, that is flushed if
you stop the application server. 

The application is based on the Jakarta EE 8, Payara Micro Maven Plugin and tested with
the Insomnia Core.

# RUN

Build the WAR artifact:
```sh
mvn package
```

Deploy the created WAR on the Payara Micro Server: 
```sh
java -jar <payara-micro.jar> --deploy <todo.war>
```

In the STDOUT you'll see something like this:

```
Payara Micro URLs:
http://192.168.0.102:8080/todo

'todo' REST Endpoints:
GET	/todo/api/v1/application.wadl
GET	/todo/api/v1/todo/list
POST	/todo/api/v1/todo/new
POST	/todo/api/v1/todo/status
PUT	/todo/api/v1/todo/update
GET	/todo/api/v1/todo/{id}
```

You can use Insomnia for working with this REST service.

# Links
Payara Micro: 
https://www.payara.fish/products/payara-micro/

Insomnia Code:
https://insomnia.rest/products/core/
