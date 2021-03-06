# FsAPI Portable Class Library
## Frontier Silicon API for .NET
 
This is an implementation of the Frontier Silicon API (FsAPI) for .NET applications.
FsAPI is used to remote control Internet / WLAN radios by [Frontier Silicon](http://www.frontier-silicon.com/)

This library is used to create a remote control application for Windows ([RadioRemote](https://www.microsoft.com/store/apps/9nblggh4qp9q)) similar to the [Android](https://play.google.com/store/apps/details?id=com.frontier_silicon.fsirc) or [iOS](https://itunes.apple.com/us/app/dok/id546270847) ones.

**Caution:** So far, this libary has only been tested with an [Dual IR6 device](http://www.dual.de/produkte/digitalradio/radio-station-ir-6) and [Sangean WFR-29C](http://www.sangean.eu/products/internet-radios/wfr-29c.html)

## Usage:

```csharp
var client = new Client(location);
var session = await client.CreateSession(pin);
var modes = client.GetRadioModes();
await client.SetVolume(10);
