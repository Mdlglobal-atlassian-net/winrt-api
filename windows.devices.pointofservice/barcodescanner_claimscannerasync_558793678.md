---
-api-id: M:Windows.Devices.PointOfService.BarcodeScanner.ClaimScannerAsync
-api-type: winrt method
---

<!-- Method syntax
public Windows.Foundation.IAsyncOperation<Windows.Devices.PointOfService.ClaimedBarcodeScanner> ClaimScannerAsync()
-->

# Windows.Devices.PointOfService.BarcodeScanner.ClaimScannerAsync

## -description
Attempts to get an exclusive access to the barcode scanner.

## -returns
When the method completes, it returns a [ClaimedBarcodeScanner](claimedbarcodescanner.md).

## -remarks

## -examples


[!code-cpp[ClaimBarcodeScanner](../windows.devices.pointofservice/code/BarcodeScanner/cpp/Scenario1.xaml.cpp#SnippetClaimBarcodeScanner)]

[!code-cs[ClaimBarcodeScanner](../windows.devices.pointofservice/code/BarcodeScanner/cs/Scenario1.xaml.cs#SnippetClaimBarcodeScanner)]

[!code-js[CreateBarcodeScannerJS](../windows.devices.pointofservice/code/BarcodeScanner/js/scenario1.js#SnippetCreateBarcodeScannerJS)]

## -see-also
[Barcode scanner sample (Windows 10)](http://go.microsoft.com/fwlink/p/?LinkId=620014)