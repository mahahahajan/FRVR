# AT&T Enhanced WebRTC JS SDK

The SDK provides the following components:

* JavaScript library - a client library to consume AT&T Enhanced WebRTC API.
* NodeJS Sample Application - Web Application to demonstrate the features
of the JavaScript library. **Please refer to [node-sample/RELEASE.md](node-sample/RELEASE.md) for Sample Applications-specific notes**.
* NodeJS Developer Hosted Server - NodeJS application to manage application assets (key, secret, etc.) and to generate OAuth access tokens and E911 Ids.
**Please refer to [node-dhs/RELEASE.md](node-dhs/RELEASE.md) for DHS-specific notes**.

# v1.0.0 - GA
December  11, 2014

* **New:** Sample application _Recipes_ link (see [node-sample/RELEASE.md](node-sample/RELEASE.md))
* **Enhancement:** When receiving a call from a Mobile Device (any service provider, e.g. Verizon, TMobile),
you can now move the call from the Browser to a AT&T Mobile Device.

## Known Issues
* Moving a mobile number to mobile device fails when there is a call between a mobile number and a non provisioned mobile device(any-network phone).
* `Phone.transfer` fails with error `Transfer terminated by Network` when the transfer target is an Account ID or Virtual Number user.
* One way audio when we add a mobile device for a video conference.
* `call:move-terminated` event is not fired when successfully completing `phone.move`.
* After successfully adding a mobile device to a Conference it will be disconnected after ~24s.
* Adding multiple participants at once using `Phone.addParticipants` method fails with error: `SVC8501:MediaConference ongoing update participant operation.,Variables=`.
* **Workaround:** Use `Phone.addParticipants` with a single participant ID (mobile number, account id, virtual number)
* When a participant leaves a conference by using the `endConference` method, the platform does not generate
the necessary event to inform the host.
* When an Mobile Number user rejects an invitation for a conference, sometimes the event `conference:ended` will not
be published due to a bug at the Platform Level.
* When adding a participant to a conference, sometimes the error: `The requested conference ID <id> was not found.`
is shown.
* Video switching between participants is sometimes inconsistent.
* **Workaround:** Turn off your microphone while the other participant speaks, that will switch the video to the
speaking participant.

## Tested Environments

* Chrome Version 39.0 for OSX v10.8.5 and Windows 8

**_The SDK may also work for other Operating Systems, other Browsers but is not tested or supported._**
