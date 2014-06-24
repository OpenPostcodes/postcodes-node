# Open Postcodes Node.js API Wrapper

Retrieve a list of addresses for any postcode in the United Kingdom using the Open Postcodes API.

## Getting Started

You can complete a full address lookup with just a couple of lines of code. Install and insert your API key, you can start immediately performing UK postcode address lookups.

**Installation**

Install using the node package manager, npm.

```bash
npm install postcodes
```

Remember to include it in package.json for portability purposes.

**Get an API Key**

Get a key at [Open Postcodes](https://openpostcodes.com), then try out our service with our testing postcodes e.g. 'XA1 0XX'

**Configuration**

You must include your API key when requiring the postcodes module. This will return an instance allowing you to perform your postcode lookups on the Open Postcodes API.

```javascript
var api_key = "your api key"
var Postcodes = require('postcodes')(api_key)
```

## Usage

Perform lookups by calling **#lookupPostode(postcode, callback)**. This function is asynchronous and so takes 2 arguments, the postcode and a callback to handle the response.

You can use the postcode "XA1 0XX" to test our service.

```javascript
Postcodes.lookupPostcode("XA1 0XX", function (error, addresses) {
	if (error) throw error; // Add error handling
	console.log(addresses);
});

// => Will output an array of addresses
//	[ {
//			postcode: 'XA1 0XX',
//			post_town: 'LONDON',
//			line_1: 'The Pavilion',
//			line_2: 'Oaks Avenue',
//			line_3: '', 
//			organisation_name: '',
//			building_name: 'The Pavilion',
// 			...truncated...
//		}, ...
```

## Signing Up

Open Postcodes provides street level address data for website, mobile and desktop applications at a competitive price.

We charge _1p_ per public lookup; take a look at our [pricing](https://openpostcodes.com/pricing)

## Documentation

More in-depth documentation can be found [here](https://openpostcodes.com/documentation#examples-nodejs)

## License
Public Domain
