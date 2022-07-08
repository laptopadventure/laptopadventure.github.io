
# Reading Notes 12

[Back to the table of contents](../../README.md)

## Reading

 * In your own words, describe what each group of status code represents:
    * 100’s
      * Informational and feedback codes, not necessarily fail codes but could be early feedback that a response is going to fail.
      * Frequently shows up with headers as early feedback that the server will process the header sent
    * 200’s
      * Success codes that things went correctly and stuff was returned, with the sole exception of 202 being a delayed response but
      everything validated correctly.
    * 300’s
      * Redirection codes. So while what was sent in was correct, what was asked for has migrated elsewhere.
    * 400’s
      * Client Errors! Something you did was wrong, some wrong key or some wrong query, etc.
    * 500’s
      * Server Errors! Something the backend did was wrong, but maybe it's more accurate to say that the backend had to reject handling it
      due to various reasons, like the servers taking on too many requests at one time to deal with, having to reject some.
 * What is a status code 202?
  * Everything is validated and looks good, but this will return something of substance in the future. Basically, async immediate success feedback, but the request isn't actually done.
 * What is a status code 308?
  * Permanent Redirect! Essentially feedback to the client that the location they're requesting from has permanently migrated to a new url they
  need to use. The previous url could be home to archived, read only data.
 * What code would you use if an update didn’t return data to a client?
  * 404, not found! It was successful, but there was nothing to grab.
 * What code would you use if a resource used to exist but no longer does?
  * 410, gone! A more permanent 'no longer here' kind of deal, and the difference from redirect is that 410 has no idea where it is now.
 * What is the ‘Forbidden’ status code?
  * 403, forbidden! If the request is expected to come with a key, and you didn't include it, that's an access problem. There could be 
  all kinds of access checks, as there are on the internet, that could block you from using an api.

# Video

Why do we need to pull our MongoDB database string out of our server and put it into our .env?
What is middleware?
What does app.use(express.json()) do?
What does the /:id mean in a route?
What is the difference between PUT and PATCH?
How do you make a default value in a schema?
What does a 500 error status code mean?
What is the difference between a status 200 and a status 201?
