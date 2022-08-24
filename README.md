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
- downloads the _"Astronomy Picture of the Day"_ image 🌌 and its explanation from the NASA website, using its [APOD API](https://api.nasa.gov/) 🚀
- zips the image and its explanation text into an archive file
- uploads the archive to a given FTP server
- 💰 _bonus_: sends a notification about the result of the upload in an email to a given address using the provided SMTP settings

### Specification

#### Requirements

* 🚀 APOD API
  * **prerequisites**: you have to generate an API key on the [website](https://api.nasa.gov/#signUp) to be able to use the API (or alternatively use the `DEMO_KEY`).
  * the program must get its API key from its input arguments
  * the program must fetch the JSON content with a standard HTTP GET request using the URL described in the documentation of the API (see the examples).
  * must be able to parse the JSON response and extract the explanation text from the `explanation` property and the image URL from the `url` property.
  * you can use any package which is available in your chosen language, or invoke a commonly used tool like `curl`
* 🗜️ Zipping
  * the explanation text must be saved into a text file with the correct encoding (UTF-8)
  * the archive file must be named in the format: `NASA_APOD_yyyyMMdd.zip`, where `yyyyMMdd` is the current date (eg.: `20220824`)
  * you can use any package which is available in your chosen language, or invoke a commonly used tool like `gzip`

### Rules & hints

* Your application's code should be uploaded to a public Git repository which you must grant access to us. Please, include README file with basic notes on application requirements and setup - we must be able to easily build and run it by ourselves.
* 🏖️ Relax, there's no time limit for the task (at least in reasonable limits). If you feel that the task is too much, you can skip some parts of it, and we will discuss how you would have done the remaining parts.

**Good luck! If you are stuck or have any questions feel free to contact us!**
