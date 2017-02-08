---
-api-id: T:Windows.Foundation.DateTime
-api-type: winrt struct
---

<!-- Structure syntax.
public struct DateTime 
-->

# DateTime

## -description
Represents an instant in time, typically expressed as a date and time of day.



> **JavaScript**
> This type appears as the [Date](XREF:TODO:ce2202bb-7ec9-4f5a-bf48-3a04feff283e) object.



> **.NET**
> When programming with .NET, this type is hidden, and developers should use the [System.DateTimeOffset](https://msdn.microsoft.com/library/system.datetimeoffset.aspx) structure.



> **C++**
> Similar to [FILETIME](XREF:TODO:base.filetime_str) but with important differences. See Remarks.

## -struct-fields

### -field UniversalTime
A 64-bit signed integer that represents a point in time as the number of 100-nanosecond intervals prior to or after midnight on January 1, 1601 (according to the Gregorian Calendar).
    

## -remarks
JavaScript and Microsoft .NET languages do not use this type directly. In JavaScript a [DateTime](datetime.md) is projected as a [Date](XREF:TODO:ce2202bb-7ec9-4f5a-bf48-3a04feff283e) object, and in Microsoft .NET it is projected as a [System.DateTimeOffset](https://msdn.microsoft.com/library/system.datetimeoffset.aspx). Each language transparently handles the conversion to the granularity and date ranges for the respective language.

In Visual C++ component extensions (C++/CX), a **DateTime.UniversalTime** value has the same granularity as a [FILETIME](XREF:TODO:base.filetime_str) (100-nanosecond intervals). For positive values, a **DateTime.UniversalTime** value is identical to a [FILETIME](XREF:TODO:base.filetime_str) value although it can only represent dates up to about 29000 C.E. A negative value represents the number of intervals prior to January 1, 1601 and can represent dates back to about 27,400 B.C.E. For the Gregorian Calendar, you can use a [DateTimeFormatter](../windows.globalization.datetimeformatting/datetimeformatter.md) to create string representations of a [DateTime](datetime.md) for dates after midnight on Year 1 C.E.

To convert the **UniversalTime** to [SYSTEMTIME](XREF:TODO:base.systemtime_str), use [ULARGE_INTEGER](http://msdn.microsoft.com/library/83a10c12-2cd1-449a-af3f-b2138fc50ee0) to convert the **int64** value to [FILETIME](XREF:TODO:base.filetime_str), then use [FileTimeToSystemTime](XREF:TODO:base.filetimetosystemtime) to get [SYSTEMTIME](XREF:TODO:base.systemtime_str).

## -examples

## -see-also
[System.DateTimeOffset](https://msdn.microsoft.com/library/system.datetimeoffset.aspx), [Date object](XREF:TODO:ce2202bb-7ec9-4f5a-bf48-3a04feff283e), [FILETIME](XREF:TODO:base.filetime_str), [Calendar sample (Windows 10)](http://go.microsoft.com/fwlink/p/?LinkId=624043)