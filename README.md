# Eficode Open Data Task 2019

synopsis: we have messed up, your task is to create a visualization. what is the data?

## Prerequisites

To access the data you need to `/signup` to our API. The signup is easy, you will send your email and a password to our signup endpoint `https://opendata.hopefully.works/api/signup`. As a return message you will receive an *accessToken*, which you will use for the subsequent requests.

Don't worry if you lose the token, you can always `/login` with your email and password to receive a new token. The login endpoint is here `https://opendata.hopefully.works/api/login`.

## The data

For this task you will have to make a request to `/events`. The event changes once per hour, and contains data from four different sensors:

```
{
  "date": "2019-01-29T22:00:00.000Z",
  "sensor1": XXX,
  "sensor2": XXX,
  "sensor3": XXX,
  "sensor4": XXX
}
```

## Your task

Your task is simply to create a visualization of the data. Return your task as code (github repository address preferred) and a webpage where we can see the results.

Can you find out what the data is?

## Hints

* To show the current event easily you might want to use a simple cloud service like [Heroku]().
* If you want to store the events and show also historical data, you will probably need a simple database.
