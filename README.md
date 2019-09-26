Aimera platform API class and examples for C#
===

In example below:
 - `api.aimera.io` - is the domain of Aimera API server. For production use api.aimera.io, for testing you may use alpha.aimera.io
 - `secret_key` - a unique key provided by Aimera to encrypt data exchange
 - `owner_id` - a unique account identifier provided by Aimera
 - `client_id` - the identifier of the client performing action. Basically phone number in international format without plus. For example client having phone number +324 123 456 has ID 324123456.
 - `event_id` - the identifier of the corresponding event in Aimera.
 - `multiple` - Optional parameter for quantifiable challenges (ex. get 1 point for every 1 euro spent). Provide value to multiple points with.

## Event tracking example

This code prepares a call to Challenger server on event happened to a client identified by {client_id}:

```C#
using ChallengerPlatform;

// ... your code ...

Challenger.setServer('api.aimera.io');
Challenger.setOwnerId('{owner_id}'); 
Challenger.setClientId('{client_id}');
Challenger.setKey('{secret_key}');
Challenger.addParam('multiple', '{multiple}'); // Optional

bool resp = Challenger.trackEvent('{event}');
```
