# Errors

<aside class="notice">This error section is stored in a separate file in `includes/_errors.md`. Slate allows you to optionally separate out your docs into many files...just save them to the `includes` folder and add them to the top of your `index.md`'s frontmatter. Files are included in the order listed.</aside>

The PartnerPath API uses the following error codes:


Error Code | Meaning
---------- | -------
400 | Bad Request -- Your request is not structure properly according to the Object operation
401 | Unauthorized -- Your API key is invalid
403 | Forbidden -- The Object requested is hidden for administrators only
404 | Not Found -- The specified Object could not be found
405 | Method Not Allowed -- You tried to access a Object with an invalid method
406 | Not Acceptable -- You requested a format that isn't json
410 | Gone -- The Object requested has been removed from our servers
429 | Too Many Requests -- The user has sent too many requests in a given amount of time.
500 | Internal Server Error -- We had a problem with our server. Try again later.
503 | Service Unavailable -- We're temporarially offline for maintanance. Please try again later.