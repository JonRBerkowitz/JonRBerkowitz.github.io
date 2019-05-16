---
layout: post
title:      "I Promise That This is About Asynchronous Requests"
date:       2019-05-16 03:55:14 +0000
permalink:  i_promise_that_this_is_about_asynchronous_requests
---


How long would you wait for a website to load? Research shows that most people's threshold is just two seconds. That's all the time that you have before the user closes that tab. Now, 1-2 seconds might be a fairly achievable mark for a standard website, but what about sites that display a lot of data, like YouTube or Instagram? How do sites like those manage to load so quickly?

The answer is asynchronous requests and promises.

**What is an asynchronous request?**
Async requests essentially allow a website to load data in the background while other things are going on. When an asynchronous get or post request is sent via a method like fetch, it returns something called a "promise." A promise is a javascipt object that may eventually return a value. It exists in one of three states, pending, fullfilled and rejected. While this promise is resolving, the other code in the application continues to execute and load.

**Types of Promises**
A pending promise is one that has not been fulfilled. That is to say, it has recieved nothing back from the initial request and is waiting to do so before it returns any data. The request that caused the pending promise may be used to put portions of the app into a "loading" state.

A fulfilled promise is one in which the expected data has been recieved, and it can now proceed to use that data, in many cases converting it into JSON and use that data to manipulate the DOM in some way. This is done via the "then()" method which will itself return a promise. This series of "then" calls can be used to further manipulate the data and handle erros.

A rejected promise is one in which the request has resolved, but without the data that it expected to recieve. From there, we can handle that rejection by throwing an error.


**Why use async?**
As mentioned earlier in this post, it can be very helpful to be able to get and post data while other tasks continue in the background. It generally makes for a better user experience when the user isn't waiting on the page to load because data retrieval has yet to complete. Async requests are a powerful tool and can be used to enhance important metrics such as load time, and overall user experience and retention.
