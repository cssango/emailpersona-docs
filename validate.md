# Validate

This method provides a simple way to validate an email address. 
It returns a JSON string with the required details. 

You will make a GET request to this endpoint: 

```
[GET] https://api.emailpersona.net/validate/{email}?api_token={token}
```

### Example Result:

```json
{
    "valid_format": true,
    "valid_mx_records": true,
    "possible_email_correction": "hello@example.com",
    "free_email_provider": false,
    "disposable_email_provider": false,
    "role_or_business_email": false,
    "valid_host": true,
    "valid_on_smtp": true
}
```

### Returned Values

| Key 							| Description 																		 |
| ----------------------------- | ---------------------------------------------------------------------------------- |
| `valid_format` 				| Indicates if the email has a valid format 										 |
| `valid_mx_records` 			| Indicates if the domain part of the email has MX records 							 |
| `possible_email_correction` 	| This suggests a correction to the provided email e.g. when there is a typo  		 |
| `free_email_provider` 		| Indicates if this email is provided by a free service e.g. yahoo.com 				 |
| `disposable_email_provider` 	| Indicates if this email is provided by a disposable email service like yopmail.com |
| `role_or_business_email` 		| Indicates if this is a role based email e.g. support@example.com  				 |
| `valid_host` 					| Indicates if the domain part of the email has a valid DNS A-record 				 |
| `valid_on_smtp` 				| Indicates if the mailbox exists on the SMTP server  								 |