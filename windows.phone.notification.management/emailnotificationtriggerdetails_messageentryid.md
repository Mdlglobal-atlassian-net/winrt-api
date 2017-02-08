---
-api-id: P:Windows.Phone.Notification.Management.EmailNotificationTriggerDetails.MessageEntryId
-api-type: winrt property
---

<!-- Property syntax
public Windows.Phone.Notification.Management.BinaryId MessageEntryId { get; }
-->

# Windows.Phone.Notification.Management.EmailNotificationTriggerDetails.MessageEntryId

## -description
Represents a unique identifier for an individual email in phone MAPI store.

## -property-value
The identifier for the email.

## -remarks
To set the right context, the app will get this as part of a new email trigger ([IEmailNotificationTriggerDetails2](http://msdn.microsoft.com/library/079905ef-a618-483f-9a52-76abee5efcbe)) as well as email read status change trigger ([IEmailReadNotificationTriggerDetails](http://msdn.microsoft.com/library/2bbeebea-de00-4baa-b9af-78b9ab8a97bb)). The [messageEntryId](emailnotificationtriggerdetails_messageentryid.md) can be used by [AccessoryManager.UpdateEmailReadStatus](accessorymanager_updateemailreadstatus.md) API to update the read status of an email identified by the entry id.

Calling this API requires that the **ID_CAP_SMS** and **ID_CAP_SMS_COMPANION** capabilities be specified in the application manifest.

## -examples

## -see-also