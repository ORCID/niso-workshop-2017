##About ORCID

**Who we are:**

- Non-profit 
- Open source project ([ORCID Github repository](https://github.com/ORCID/ORCID-Source))
- Committed international community

**Our goal:**

All who participate in research, scholarship, and innovation are **uniquely identified** and **connected to their contributions** across disciplines, borders, and time.

**What we provide:**

- **Persistent digital identifier** for researchers (ORCID iD):<br>[https://orcid.org/0000-0001-5727-2427](https://orcid.org/0000-0001-5727-2427)
- **Registry** of those identifiers + their connections to affiliations and research activities
- **APIs** for creating/retrieving metadata about connections between people, affiliations and research activities

**Why?**

- Help people find information (like all of a researcher's publications)
- Simplify reporting and analysis (by providing a central source for info about researcher's affilations and activiteis)
- Reduce time spent filling out forms (by providing a source for autopopulating form fields)


ORCID doesn't do this on its own - integrations with other systems (like manuscript submission/production, funding application, repository, research information, and directory systems) are essential.

##About the ORCID APIs
ORCID's web interface gives researchers a way to interact with their record, but the real power of ORCID lies in the underlying data, which can be accessed by people and systems via Application Programming Interfaces (APIs).

* **Public API:** Free to anyone with an ORCID iD
* **Basic Member API:** Available to ORCID member organizations who subscribe at the Basic level (Sandbox Member API freely available for testing)
* **Premium Member API:** Available to ORCID member organizations who subscribed at the Premium level (Sandbox Premium Member API freely available for testing)

[Learn more about membership levels](https://orcid.org/about/membership)<br><br>


| Features       | Public | Basic Member | Premium Member |
| -------------- | ---------- | ---------------- | ------------------ |
|**READ**<br>Read data ORCID records| **X**<br>*Public data*  | **X**<br>*Public + limited-access data (with user permission)* | **X**<br>*Public + limited-access data (with user permission)* |
|**SEARCH**<br>Search data on ORCID records| **X**<br>*Public data* | **X**<br>*Public data*  | **X**<br>*Public data* |
|**AUTHENTICATE**<br>Get a user's authenticated ORCID iD| **X** | **X** | **X** |
|**UPDATE**<br>Add items to a record or update items you added previously|  | **X** | **X** |
|**WEBHOOKS**<br>Get notifications when ORCID records you're monitoring are updated|  |  | **X** |

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