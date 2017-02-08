---
-api-id: T:Windows.Networking.NetworkOperators.MobileBroadbandNetworkRegistrationStateChangeTriggerDetails
-api-type: winrt class
---

<!-- Class syntax.
public class MobileBroadbandNetworkRegistrationStateChangeTriggerDetails : Windows.Networking.NetworkOperators.IMobileBroadbandNetworkRegistrationStateChangeTriggerDetails
-->

# Windows.Networking.NetworkOperators.MobileBroadbandNetworkRegistrationStateChangeTriggerDetails

## -description
Provides details for a network registration state change notification.

This functionality is only available to mobile operator apps and Windows Store app given privileged access by mobile network operators. For more information, see [Mobile Broadband: ](http://msdn.microsoft.com/library/windows/hardware/hh852368.aspx).

## -remarks
When a background task is triggered by a mobile network registration state change notification, the [IBackgroundTaskInstance.TriggerDetails](../windows.applicationmodel.background/ibackgroundtaskinstance_triggerdetails.md) property returns an instance of this class with information specific to the triggered notification.

The operating system extends battery life by suspending applications that are not in the foreground. If your application must handle new network registration state change notifications even while suspended, you must create a background work item to handle the messages. When a new network registration state change notification arrives, the background work item will be activated. The [MobileBroadbandNetworkRegistrationStateChangeTriggerDetails](mobilebroadbandnetworkregistrationstatechangetriggerdetails.md) class provides the details of the event to your background work item code.

## -examples

## -see-also