Aimera platform API class and examples for C#
===

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
