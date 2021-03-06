﻿# Configure SMS sending - Amplia

If users will issue certificates (either web or mobile issuing procedure), a SMS confirmation is required to confirm the identity of the user during the
certificate issue procedure. SMS messages may be sent using different *providers*.

The section **SMS** of the JSON configuration file configures the SMS sending. The setting **Type** defines which provider should be used, and the remaining settings depend on the provider chosen:

* [Twilio](https://www.twilio.com/)
  * **Type**: set this setting to `Twilio` to send SMS messages using Twilio
  * **MessageFrom**: the sender phone number provided by Twilio (e.g.: `+12125550000`)
  * **AccountSid**: the account SID, provided by Twilio
  * **AuthToken**: the authentication token, provided by Twilio
* [TotalVoice](https://totalvoice.com.br/)
  * **Type**: set this setting to `TotalVoice` to send SMS messages using TotalVoice
  * **AccessToken**: the access token, provided by TotalVoice (e.g.: `0123456789abcdef0123456789abcdef`)
* Simulator (for debugging purposes only)
  * **Type**: set this setting to `Simulator` to simulate sending SMS messages (messages that would be sent are only logged)

## See also

* [Amplia on-premises](index.md)
