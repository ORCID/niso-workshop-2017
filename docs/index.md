##About the ORCID APIs
ORCID's web interface gives researchers a way to interact with their record, but the real power of ORCID lies in the underlying data, which can be accessed by people and systems via Application Programming Interfaces (APIs).

* **Public API:** Free to anyone with an ORCID iD
* **Basic Member API:** Available to ORCID member organizations who subscribe at the Basic level (Sandbox Member API freely available for testing)
* **Premium Member API:** Available to ORCID member organizations who subscribed at the Premium level (Sandbox Premium Member API freely available for testing)

[Learn more about membership levels](https://orcid.org/about/membership)<br><br>


| Features       | Public | Basic Member | Premium Member |
| -------------- | ---------- | ---------------- | ------------------ |
|**AUTHENTICATE**<br>Get a user's authenticated ORCID iDs| X | X | X |
|**READ(PUBLIC)**<br>Read/search public data on ORCID records| X | X | X |
|**READ (LIMITED)**<br>Read/search limited-access data on ORCID records|  | X | X |
|**UPDATE**<br>Add items to a record or update items you added previously|  | X | X |
|**WEBHOOKS**<br>Get notifications when ORCID records you're monitoring are updated|  |  | X |

All of the ORCID APIs are  based on the same set of technologies:

* **REST:** ORCID APIs are &ldquo;RESTful&rdquo;, which  means that they use HTTP to transfer information.
* **OAuth:** ORCID  APIs use the [OAuth 2.0 authentication protocol](https://oauth.net/2/) to grant client  applications access to users&rsquo; ORCID records.
* **XML/JSON:** ORCID APIs support data exchange in either XML or JSON format.

[Learn more about the ORCID APIs](https://members.orcid.org/api/about-orcid-apis)

##Pre-requisites
To complete this tutorial, you'll need the following tools:

* **Web browser:** Firefox (33+), Chrome (38+), Internet Explorer (10+), Safari (6+)
* **Internet connection**
* **Plain text editor:** TextEdit (Mac), Notepad++ (Win), or your preferred plain text editor
* **Software capable of making HTTP requests:**
    - [cURL](http://curl.haxx.se/download.html): Free, command-line application available for Mac  or Windows (pre-installed on most Mac OS versions; accessible within Terminal application)
    - GUI tools, like [Postman](https://www.getpostman.com/), [Google OAuth Playground](https://developers.google.com/oauthplayground/) or [hurl.it](http://hurl.it">hurl.it)

Examples in this tutorial use [Postman](https://www.getpostman.com/)