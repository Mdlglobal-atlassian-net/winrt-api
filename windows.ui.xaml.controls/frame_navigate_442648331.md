---
-api-id: M:Windows.UI.Xaml.Controls.Frame.Navigate(Windows.UI.Xaml.Interop.TypeName)
-api-type: winrt method
---

<!-- Method syntax
public bool Navigate(Windows.UI.Xaml.Interop.TypeName sourcePageType)
-->

# Windows.UI.Xaml.Controls.Frame.Navigate

## -description
Causes the [Frame](frame.md) to load content represented by the specified [Page](page.md).

## -parameters
### -param sourcePageType
The page to navigate to, specified as a type reference to its partial class type. (A type reference is given as [System.Type](https://msdn.microsoft.com/library/system.type.aspx) for Microsoft .NET, or a [TypeName](../windows.ui.xaml.interop/typename.md) helper struct for Visual C++ component extensions (C++/CX)).

## -returns
**false** if a [NavigationFailed](frame_navigationfailed.md) event handler has set [Handled](../windows.ui.xaml.navigation/navigationfailedeventargs_handled.md) to **true**; otherwise, **true**. See Remarks for more info.

## -remarks
You handle the [NavigationFailed](frame_navigationfailed.md) event to respond to navigation failure. You can handle the failure directly in the event handler, or you can set the [NavigationFailedEventArgs.Handled](../windows.ui.xaml.navigation/navigationfailedeventargs_handled.md) property to **true** and use the [Navigate](frame_navigate.md) method return value to respond to the failure.

Apps typically use [GetNavigationState](frame_getnavigationstate.md) to serialize the frame’s state when the app suspends. You can do this directly in your app code or indirectly by using the `SuspensionManager` class generated by the Visual Studio templates. To enable frame state serialization using [GetNavigationState](frame_getnavigationstate.md), you must use only basic types for the navigation parameter, such as string, char, numeric, and GUID types. Otherwise [GetNavigationState](frame_getnavigationstate.md) will throw an exception when the app suspends. The parameter can have other types if you do not use [GetNavigationState](frame_getnavigationstate.md).

The parameter value can have a complex type if you do not use [GetNavigationState](frame_getnavigationstate.md). However, you should still use only basic types in order to avoid excess memory usage caused by the frame’s navigation stack holding a reference to the parameter. A preferred approach is to not pass the actual object, but instead pass an identifier that you can use to look up the object in the target landing page. For example, instead of passing a `Customer` object, pass a reference to the `CustomerID`, then look up the `Customer` after the navigation is complete.

> [!TIP]
> If you are programming using a Microsoft .NET language (C# or Microsoft Visual Basic), the [TypeName](../windows.ui.xaml.interop/typename.md) type projects as [System.Type](https://msdn.microsoft.com/library/system.type.aspx). When programming using C#, it is common to use the **typeof** operator to get references to the [System.Type](https://msdn.microsoft.com/library/system.type.aspx) of a type. In Microsoft Visual Basic, use **GetType**. If you're using Visual C++ component extensions (C++/CX), where you'll need to create a [TypeName](../windows.ui.xaml.interop/typename.md) helper struct, you can use the [typeid component extension](XREF:TODO:e9706cae-e7c4-4d6d-b474-646d73df3e70).

## -examples

## -see-also
[Page](page.md), [Navigate(Type, Object)](frame_navigate_1603787821.md), [NavigationFailed](frame_navigationfailed.md), [Navigation](http://msdn.microsoft.com/library/742c1c18-c7b1-47b7-866c-726eeb8235ec), [XAML Navigation sample](http://go.microsoft.com/fwlink/p/?LinkID=330214)