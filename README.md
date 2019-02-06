# Eficode Open Data Task 2019

We at Eficode had a good will to create a system that would report a certain sensor data over around the internet. The result is a service that returns changing sensor data every hour.

What we were not able to, was to show any visualization of the data, nor were we able to show any history of the information collected. For this, **we need your help**.

## Prerequisites

To access the data you need to `/api/signup` to our API. The signup is easy; you **POST** your email and a password **as JSON** in the request body into our signup endpoint `https://opendata.hopefully.works/api/signup`. As a return message you will receive an **accessToken**, which you will have to use for the subsequent requests.

```
POST /api/signup
Content-type: application/json
{ "email": "your.email@address", "password": "yourselectedpassword" }
```

Don't worry if you lose the token, you can always `/api/login` with your email and password to receive a new token. The login endpoint is here `https://opendata.hopefully.works/api/login`, and works with the same request body in JSON format.

## The data

For this task you will have to make a request to `/api/events` to receive the JSON response below. The event changes once per hour, and contains data from four different sensors.

To be able to access the `/api/events`, you will have to set a request header using the **accessToken** you received when signing up (or logging in): `Authorization: Bearer <your accessToken>`.

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

Your task is to create a visualization of the data. Return your task as code ([github](https://www.github.com) repository address preferred) and a webpage from which we can see your visualization of the data.

Ah yes, and by the way can you find out what the data is?

## Hints

* If you have no idea what to do, you might want to use a simple cloud service like [Heroku](https://www.heroku.com/).
* If you want to store the events and show also historical data, you will probably need a simple database.
* Our magic words are [react](https://reactjs.org/), [nodejs](https://nodejs.org) and [docker](https://www.docker.com/), but don't want limit your selected tech stack in any way.
