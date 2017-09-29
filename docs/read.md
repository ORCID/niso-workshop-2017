In this section, we'll use the Public API to take a look at the underlying data for our Sandbox record. For more details on this process, see our [Basic tutorial: Read data on an ORCID record ](http://members.orcid.org/api/tutorial/read-orcid-records)

##Get an access token
Reading and searching public data on ORCID records requires an [OAuth 2.0](https://oauth.net/2/) access token obtained using a **client credentials** grant type.

This type of token can be re-used many times to read or search any ORCID records.

1. In the Postman Builder tab, click **Authorization**, then set the **Type** dropdown to **OAuth 2.0**<br> 
<img src="../images/04-2_auth-type.png" width="600" alt="Postman authorization type config" />
3. Click **Get New Access Token**
2. Enter the following settings:


| Field | Value |
| ------| ------|
|**Token Name**| Read public |
|**Auth URL**| Leave blank |
|**Access Token URL**| ```https://sandbox.orcid.org/oauth/token``` |
|**Client ID**| ```APP-XA6KUTFCVQL0622C```<br>(Demo client ID created for this workshop) |
|**Client Secret**| ```7c8d6b1b-401b-4f5d-9b8b-b8108c6e197c```<br>(Demo client secret created for this workshop - do not share API client secrets!) |
|**Scope**| ```/read-public``` <br>This scope allows reading or searching public data on any ORCID records [ORCID Scopes](https://members.orcid.org/api/oauth/orcid-scopes)|
|**Grant Type**| Client Credentials|

3. Leave **Request access token locally** unchecked and click **Request Token**<br>
<img src="../images/read-public-token-config.png" width="400" alt="Postman config for client credentials token" />
4. Beneath **Existing Tokens**, click **Read public**. The access token will appear at right. Notice that the token expires in 
631138518 sec (20 years), which means that this token can be reused for some time. <br>
<img src="../images/read-public-token-response.png" width="600" alt="Postman response for an access token request" /><br>

##Read a record summary
1. Set the request type to **GET**
2. In the **Enter request URL** field enter:<br>
```https://pub.sandbox.orcid.org/v2.0/0000-0002-4456-8947/record```<br>
*Replace the ORCID iD above with the iD for your Sandbox record, format XXXX-XXXX-XXXX-XXXX*<br>
<img src="../images/02-1_request-record.png" width="600" alt="Postman request for ORCID record summary" />
3. Click **Send**
4. A summary version of your record in XML format will appear in the **Body** section of the response<br>
<img src="../images/02-1_response-record.png" width="600" alt="Postman response for ORCID record summary" />

##Read activity details
To get more information about a specific item on an ORCID record, you can retrieve that individual item using its put-code.

1. In the record summary XML, find the **activities-summary** section, then find the **put-code** for the employment item that you added in the previous section.<br>
<img src="../images/02-2_put-code.png" width="600" alt="XML showing put-code for an employment item on an ORCID record" />
2. In the **Request URL** field enter:<br>
```https://pub.sandbox.orcid.org/v2.0/0000-0002-4456-8947/employment/26970```<br>
*Replace [ORCID ID] with the iD for your Sandbox record, format XXXX-XXXX-XXXX-XXXX and the put-code with the put-code for your employment item*<br>
<img src="../images/02-2_request-employment.png" width="600" alt="Postman request for an employment item on an ORCID record" />
3. Click **Send**
4. Fulls details of your employment entry will appear in the **Body** of the response section<br>
<img src="../images/02-2_response-employment.png" width="600" alt="Postman response an employment item on an ORCID record" />