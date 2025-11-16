# app

Option	Type	Description
allowlist	Array of strings	If included, denylist will be ignored and all parameters but those in this list will be redacted.
baseLogUrl	string	This value is used when building the x-documentation-url header (see docs below). It is your ReadMe documentation's base URL (e.g. https://example.readme.com). If not provided, we will make one API call a day to determine your base URL (more info in Documentation URL. If provided, we will use that value and never look it up automatically.
bufferLength	number	Defaults to 1. This value should be a number representing the amount of requests to group up before sending them over the network. Increasing this value will increase performance but delay the time until logs show up in the dashboard. The default value is 1.
denylist	Array of strings	An array of parameter names that will be redacted from the query parameters, request body (when JSON or form-encoded), response body (when JSON) and headers. For nested request parameters use dot notation (e.g. a.b.c to redact the field c within { a: { b: { c: 'foo' }}}).
development	bool	Defaults to false. When true, the log will be marked as a development log. This is great for separating staging or test data from data coming from customers.
fireAndForget	bool	Defaults to true. When false, the server will wait for the response from the metrics call. This will be slower, but the response is useful in debugging problems.
