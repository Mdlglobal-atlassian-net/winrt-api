---
-api-id: P:Windows.ApplicationModel.Activation.ContactMessageActivatedEventArgs.ServiceId
-api-type: winrt property
---

<!-- Property syntax
public string ServiceId { get; }
-->

# Windows.ApplicationModel.Activation.ContactMessageActivatedEventArgs.ServiceId

## -description
Gets the identifier of the service used for the message.

## -property-value
The identifier of the service used for the message.

## -remarks
For standard text messages, the ServiceId property is set to "telephone." For web service-based messaging, the ServiceId property is set to the domain name of the service to be used for messaging, for example “skype.com”. Your app will only receive message activations for ServiceIds that match the "ServiceId" elements that your app has registered in its manifest.

For info about how to handle app activation through contact actions, see [Quickstart: Handling contact actions ](https://docs.microsoft.com/previous-versions/windows/apps/dn518236(v=win.10)) and [Quickstart: Handling contact actions ](https://docs.microsoft.com/previous-versions/windows/apps/dn518338(v=win.10)).

## -examples

## -see-also
[Handling Contact Actions sample](http://code.msdn.microsoft.com/windowsapps/Handling-Contact-Actions-359380e2)
