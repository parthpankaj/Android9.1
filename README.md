# Android9.1
What is the difference between Internal Storage & External Storage?
	Store private data on the device memory.Store public data on the shared external storage..
files saved to the internal storage are private to your application and other applications cannot access them (nor can the user). When the user uninstalls your application, these files are removed.

To create and write a private file to the internal storage:

Call openFileOutput() with the name of the file and the operating mode. This returns a FileOutputStream.
Write to the file with write().
Close the stream with close().

Every Android-compatible device supports a shared "external storage" that you can use to save files. This can be a removable storage media (such as an SD card) or an internal (non-removable) storage. Files saved to the external storage are world-readable and can be modified by the user when they enable USB mass storage to transfer files on a computer.




For how long the data resides in the cache?
When the device is low on internal storage space, Android may delete these cache files to recover space.you should not rely on the system to clean up these files for you. You should always maintain the cache files yourself and stay within a reasonable limit of space consumed, such as 1MB. When the user uninstalls your application, these files are removed.




What are the critical Permissions and Normal Permissions? What are the examples of each?
Normal Permissions.

ACCESS_LOCATION_EXTRA_COMMANDS
ACCESS_NETWORK_STATE
ACCESS_NOTIFICATION_POLICY
ACCESS_WIFI_STATE
BLUETOOTH
BLUETOOTH_ADMIN
BROADCAST_STICKY
CHANGE_NETWORK_STATE. 


Critical Permissions.
Android runs each app in a limited access sandbox. If the app wants to use resources or information outside of its sandbox, the app has to explicitly request permission. Depending on the type of permission the app requests, the system may grant the permission automatically, or the system may ask the user to grant the permission.
