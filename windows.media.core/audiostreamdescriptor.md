---
-api-id: T:Windows.Media.Core.AudioStreamDescriptor
-api-type: winrt class
---

<!-- Class syntax.
public class AudioStreamDescriptor : Windows.Media.Core.IAudioStreamDescriptor, Windows.Media.Core.IAudioStreamDescriptor2, Windows.Media.Core.IMediaStreamDescriptor
-->

# Windows.Media.Core.AudioStreamDescriptor

## -description
Represents a description an audio media stream.

## -remarks
When creating a [MediaEncodingProfile](../windows.media.mediaproperties/mediaencodingprofile.md), call [SetAudioTracks](../windows.media.mediaproperties/mediaencodingprofile_setaudiotracks_1151007226.md), passing in one or more **AudioStreamDescriptor** objects to provide information about the audio tracks to be encoded.

See the [MediaStreamSource Sample](http://code.msdn.microsoft.com/windowsapps/MediaStreamSource-media-dfd55dff) for an example of using Media Stream Source in a UWP app.

### Version history

| Windows version | SDK version | Value added |
| -- | -- | -- |
| 1607 | 14393 | LeadingEncoderPadding |
| 1607 | 14393 | TrailingEncoderPadding |
| 1709 | 16299 | Label |
| 1803 | 17134 | Copy |

## -examples

## -see-also
[IMediaStreamDescriptor](imediastreamdescriptor.md), [MediaStreamSource Sample](http://code.msdn.microsoft.com/windowsapps/MediaStreamSource-media-dfd55dff)
