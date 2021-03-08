## Day 02

Working on [mailgun](https://login.mailgun.com/login/)

I've find how to send email

```javascript
const mailgun = require("mailgun-js");
const DOMAIN = 'YOUR_DOMAIN_NAME';

const mg = mailgun({apiKey: api_key, domain: DOMAIN});
const data = {
	from: 'Excited User <me@samples.mailgun.org>',
	to: 'bar@example.com, YOU@YOUR_DOMAIN_NAME',
	subject: 'Hello',
	text: 'Testing some Mailgun awesomness!'
};

mg.messages().send(data, function (error, body) {
	console.log(body);
});

```

I now how to setup a domain.
My domain were brought on Vercel plateform, and setting up the dns is pretty easy.
Unfortunatly using the free plan we can't receive email on mailgun plateform. 
