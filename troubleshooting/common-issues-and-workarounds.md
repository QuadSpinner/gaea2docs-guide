---
icon: suitcase-medical
---

# Common Issues and Workarounds

## Gaea fails to start. \[Missing Runtime]

You may be missing the Microsoft .NET Runtime. Install it [from this link](https://dotnet.microsoft.com/en-us/download/dotnet/thank-you/runtime-desktop-8.0.17-windows-x86-installer), then try again. This may be particularly possible with Portable installations.

If it still does not work, you may be missing a necessary C++ runtime. This may be particularly possible with Portable installations. Try installing the [latest Visual C++ runtime](https://aka.ms/vs/17/release/vc_redist.x64.exe).

***

## Gaea fails or freezes on starting up. \[NVidia GPU / Nahimic]

#### Nvidia Drivers

Some users have reported issues with recent NVidia GPU drivers. We recommend trying an [older driver such as 566](https://www.nvidia.com/en-us/drivers/details/237726/)

#### Nahimic / SteelSeries Conflict

The "Nahimic" audio utility is installed with software bundles from manufacurers such as ASUS, MSI, etc. This audio tweaking application can aggressively interfere with non-game applications.

With Gaea, it can prevent the 3D viewport from launching successfully and force Gaea into a 2D-only view.

We highly recommend either excluding Gaea from this and other utilities that may inject code or interject themselves into Gaea's functionality, or disable/uninstall it completely.

Please look at the following resources for further information and details on uninstalling.

[Uninstalling Nahimic](https://dovidenko.com/2021/1233/nahimic-uninstalling-blocking-msi-bloatware.html)

[Microsoft Community](https://answers.microsoft.com/en-us/windows/forum/all/nahimic-companion-keeps-reinstalling/31885fb6-7fbc-403f-827b-b1abfb6fddde)

[Google](https://www.google.com/search?q=uninstall+Nahimic)

***

## Erosion does not work or viewport does not render properly, but the rest of the application works.

You may be missing a necessary C++ runtime. This may be particularly possible with Portable installations.\
\
Try installing the [latest Visual C++ runtime](https://aka.ms/vs/17/release/vc_redist.x64.exe).

***

## I get a GRPC or other error when trying to activate my license.

Make sure your firewall is configured to allow TCP access to <kbd>https://\*.quadspinner.com</kbd> using ports <kbd>80 / HTTP</kbd> and <kbd>443 / HTTPS</kbd>.

***

## Other issues with activation.

Sometimes if you have excessive activations, this may happen.\
\
Try to log into your [User Account](https://quadspinner.com/Account) and see if there are any older or obsolete activations for your license. Removing them, and then reloading your license key in Gaea should fix the issue.

