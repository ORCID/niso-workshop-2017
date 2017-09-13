In this section, we'll use the Public API to take a look at the underlying data for our Sandbox record. 

##Read a record summary
1. Open Postman and click the **Builder** tab at the top of the screen
2. Set the request type to **GET**
3. In the **Enter request URL** field enter:<br>
```https://pub.sandbox.orcid.org/v2.0/[ORCID ID]/record```<br>
*Replace [ORCID ID] with the iD for your Sandbox record, format XXXX-XXXX-XXXX-XXXX*<br>
<img src="../images/02-1_request-record.png" width="600" alt="Postman request for ORCID record summary" />
4. Click **Send**
5. A summary version of your record in XML format will appear in the **Body** section of the response<br>
<img src="../images/02-1_response-record.png" width="600" alt="Postman response for ORCID record summary" />

##Read activity details
To get more information about a specific item on an ORCID record, you can retrieve that individual item using its put-code.

1. In the record summary XML, find the **activities-summary** section, then find the **put-code** for the employment item that you added in the previous section.<br>
<img src="../images/02-2_put-code.png" width="600" alt="XML showing put-code for an employment item on an ORCID record" />
2. In the **Request URL** field enter:<br>
```https://pub.sandbox.orcid.org/v2.0/[ORCID ID]/employment/[PUT CODE]```<br>
*Replace [ORCID ID] with the iD for your Sandbox record, format XXXX-XXXX-XXXX-XXXX and [PUT CODE] with the put-code for your employment item*<br>
<img src="../images/02-2_request-employment.png" width="600" alt="Postman request for an employment item on an ORCID record" />
3. Click **Send**
4. Fulls details of your employment entry will appear in the **Body** of the response section<br>
<img src="../images/02-2_response-employment.png" width="600" alt="Postman response an employment item on an ORCID record" />