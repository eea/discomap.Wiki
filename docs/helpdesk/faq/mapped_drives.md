# Folder registering error

## Avoiding Mapped Network Drives for ArcGIS Server

Using mapped network drives for registering folders in ArcGIS Server can lead to path resolution issues and server unawareness. Always use the full network path to ensure consistent and reliable access.
This guide explains why using mapped network drives can cause issues and how to avoid them.

**Path Resolution Problems:**
Mapped drives are essentially shortcuts created on a user's local machine. The server cannot resolve these shortcuts to the actual network locations without having the same mappings.
Using full network paths ensures consistency and is universally accessible from any machine or service within the network, making it a reliable method for data registration.

**Recommended Practice:**
To avoid issues when registering folders to ArcGIS Server, always use the full network path within the ArcGIS Pro environment instead of mapped network drives.

Example of Mapped Drive Path: Z:\folder
Example of Full Network Path: `\\cwsfileserver.eea.dmz1\folder`

When registering a folder in ArcGIS Server, enter the full path:
`\\cwsfileserver.eea.dmz1\folder`