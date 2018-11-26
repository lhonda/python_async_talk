# async talk

This project is an example on how we can decouple time consuming processes from http requests.

The idea is to present an example using Celery, Rabbitmq, Flask, jwt and jsonapi.

Also I'd like to use events to show how to create a way to make sure a transaction using micro services could work.

For instance, let's say an order is created and the user microservice must be notified about ths order creation.

I assume each microservice has its own database.

Also we need an event history so we can debug any issues and replay a set of events; these evenths imply that we know beforehand the state table of all entities.

The microservice must know what to do in case of remote failure so it sends a proper response to the client.
