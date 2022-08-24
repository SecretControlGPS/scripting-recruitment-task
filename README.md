# Recruitment task

👋 Hello!

Welcome to your test assignment for the position of sysadmin / devops engineer at 🚩 **Secret Control GPS**.
Below you can find the requirements defined for the task to complete, where you can use any of the following
languages (in order of our precedence of flavour):
- Python
- Go
- Javascript (on NodeJs)

### Overview

We need a small command-line tool for some kind of automation which does several tasks as follows:
- downloads the _"Astronomy Picture of the Day"_ image from the NASA website, using its [APOD API](https://api.nasa.gov/).
- renames the image in the format of "NASA_APOD_<yyyyMMdd>.<extension>"
- uploads the image to a given FTP server
- sends the image and its explanation in an email to a given address using the provided SMTP settings

### Specification

#### Requirements

Create a REST API which implements the following endpoints:

* `POST /movies`:
  * Must store a new movie in the database if does not exist. The movie title is enough in the request body.
  * Additional movie details should be fetched from http://www.omdbapi.com/ and persisted to database.<br>
    (At least save these fields: `Title`, `Year`, `Genre`, `Actors`, `Poster`, `imdbRating` - will be needed by the frontend).
  * Response should contain the additional fields fetched from the external API.
* `GET /movies`:
  * Must return all movies stored in the database.
  * 🦸 _Implementing filtering, sorting is a bonus._
* `POST /reviews`:
  * Request must contain the movie ID (already present in database) and the review text in its body.
  * The review has to be persisted to database and returned in the response.
* `GET /reviews`:
  * Must list all existing reviews from the database.
  * Should support filtering on movie ID.

### Rules & hints

* Your application's code should be uploaded to a public Git repository which you must grant access to us. Please, include README file with basic notes on application requirements and setup - we must be able to easily build and run it by ourselves.
* 🏖️ Relax, there's no time limit for the task (at least in reasonable limits). If you feel that the task is too much, you can skip some parts of it, and we will discuss how you would have done the remaining parts.

**Good luck! If you are stuck or have any questions feel free to contact us!**
