# Read: 26 - Android Fundamentals

- Android apps can be written using Kotlin, Java, and C++ languages.

- Each Android app, protected by the following Android security features:
1. The Android operating system is a multi-user Linux system in which each app is a different user.
2. By default, the system assigns each app a unique Linux user ID (the ID is used only by the system and is unknown to the app). The system sets permissions for all the files in an app so that only the user ID assigned to that app can access them.
3. Each process has its own virtual machine (VM), so an app's code runs in isolation from other apps.
4. By default, every app runs in its own Linux process. The Android system starts the process when any of the app's components need to be executed, and then shuts down the process when it's no longer needed or when the system must recover memory for other apps.


- The Android system implements the principle of least privilege. That is, each app, by default, has access only to the components that it requires to do its work and no more. 

- It's possible to arrange for two apps to share the same Linux user ID, in which case they are able to access each other's files. 

- An app can request permission to access device data. The user has to explicitly grant these permissions. 


## App components


