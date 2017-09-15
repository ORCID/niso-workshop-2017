In a real-world situation, you may need to update information that you've added previously, like the dates of a researcher's affiliation with your institution. 

In this section, we'll use the Sandbox Member API to update our education affiliation to include an end date.

##Update an education affiliation

1. In the **Response** section from the POST request we just made, click **Headers** and scroll down to **Location**. Copy the 5-character code at the end of the URI - this is the **put-code** for the education affiliation that you added in the previous section.<br>
<img src="../images/06-2_put-code.png" width="600" alt="Detailed view of Postman response for successful education affiliation POST request showing put-code" />
2. At the top of the screen, set the request type to **PUT**<br>
3. In the **Request URL** field, add a ```/``` to the end of the URL and paste the put code after it. The full URL should be:<br>
```https://api.sandbox.orcid.org/v2.0/[ORCID ID]/education/[PUT CODE]```<br>
*Replace [ORCID ID] with the iD for your Sandbox record, format XXXX-XXXX-XXXX-XXXX and [PUT CODE] with the put-code for your education affiliation*<br>
<img src="../images/06-2_request-uri.png" width="600" alt="Postman request URI configuration for updating an education affiliation" />
4. Click **Authorization** and make sure that your **Update record** token is still selected, and the **Add token to** dropdown is still set to **Header**<br>
<img src="../images/06-1_authorization.png" width="600" alt="Postman authorization config for education affiliation POST request" />
5. Click **Headers** and make sure that ```accept``` and ```Content-type``` are both set to ```application/vnd.orcid+xml```<br>
<img src="../images/06-2_put-headers.png" width="600" alt="Postman header configuration" />
6. Click **Body**; the XML for the affiliation you added in the previous step should appear.
7. Inside the ```<education:education``` tag, add ```put-code="[PUT CODE]"```<br>
*Replace [PUT CODE] with the put-code for your education affiliation, ex ```<education:education put-code="26971"```*<br>
<img src="../images/06-2_request-body-1.png" width="600" alt="Postman request body configuration for updating an education affiliation showing where to place put-code" />
8. Copy the [affiliation end date XML](#affiliation-end-date-xml) at the end of this section and paste it beneath the ```</common:start-date>``` tag (and above the ```<education:organization>``` tag)<br>
<img src="../images/06-2_request-body-2.png" width="600" alt="Postman request body configuration for updating an education affiliation showing where to place end-date XML" />
9. Click **Send**.
10. The  results will appear in the **Response** at the bottom of the screen. If you see **Status: 200 OK**, your education affiliation was successfully updated!<br>
<img src="../images/06-2_put-affiliation-response.png" width="600" alt="Postman response for successful education affiliation PUT request" /><br>
***Got an error?** Check the [ORCID API error code reference](http://members.orcid.org/api/resources/error-codes) for help*
11. Visit the **public  view** of your Sandbox record at ```http://sandbox.orcid.org/[ORCID ID]``` to see your updated education affiliation.<br>
<img src="../images/06-2_updated-affiliation.png" width="600" alt="ORCID record with updated education affiliation item" /><br>

##Affiliation end date XML

```
<common:end-date>
  <common:year>2017</common:year>
  <common:month>01</common:month>
  <common:day>31</common:day>
</common:end-date>
```
