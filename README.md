# sms_forwarder-server

Server side application that can use an 3rd party API to receive SMS and safe it locally. 

It also offers an API for other applications to retrieve the saved SMS (of parts of it).

## Implementations details

### Incoming API

Recieve webhooks from SMS providers to ingest SMS.
As the SMS providers don't all have the same format, being able to specify the parameters as a parameter itself would be nice.

### Outgoing API

Reply to requests for SMS to a specific number.
Requests include a _number_ and a _unique id_.
Only deliver SMS that were reveived _after_ the first request for a unique id.

### Potential SMS providers

- [Twilio](https://www.twilio.com/docs/sms/tutorials/how-to-receive-and-reply)
- [infobip](https://dev.infobip.com/receive-sms)
- [TextMagic](https://www.textmagic.com/docs/api/receive-sms/)
- [Clockwork](https://www.clockworksms.com/doc/easy-stuff/http-interface/receive-sms/)
- [nexmo](https://developer.nexmo.com/messaging/sms/building-blocks/receiving-an-sms)
- [clickatel](https://www.clickatell.com/products/sms-api/)
- and probably many more
