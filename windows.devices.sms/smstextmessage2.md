---
-api-id: T:Windows.Devices.Sms.SmsTextMessage2
-api-type: winrt class
---

<!-- Class syntax.
public class SmsTextMessage2 : Windows.Devices.Sms.ISmsMessageBase, Windows.Devices.Sms.ISmsTextMessage2
-->

# Windows.Devices.Sms.SmsTextMessage2

## -description
Encapsulates a decoded SMS text message. Prefer this class to the older [SmsTextMessage](smstextmessage_smstextmessage.md) class.

> [!NOTE]
> This functionality is only available to mobile operator apps and Windows Store app given privileged access by mobile network operators, mobile broadband adapter IHV, or OEM. For more information, see [Mobile Broadband:  device apps](http://msdn.microsoft.com/library/windows/hardware/hh852368.aspx).

To send a text message, construct an instance of this class, set all appropriate fields, and send using [SmsDevice2.SendMessageAndGetResultAsync](smsdevice2_sendmessageandgetresultasync.md).

To access a received text message, create a background task that is triggered by the SmsMessageReceived event. In that task, first use [SmsMessageReceivedTriggerDetails.MessageType](smsmessagereceivedtriggerdetails_messagetype.md) to determine that the message is a text message, then use the [SmsMessageReceivedTriggerDetails.TextMessage](smsmessagereceivedtriggerdetails_textmessage.md) property to access the instance of this class.

## -remarks

## -examples

## -see-also
[ISmsMessageBase](ismsmessagebase.md)

## -capabilities
cellularMessaging