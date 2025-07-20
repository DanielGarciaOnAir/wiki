# Polycom VVX-4xx/5xx

![PolyVVX-401_Phone "Polycom VVX-401"](https://user-images.githubusercontent.com/40501228/186971221-e9fd9166-ddc9-43d0-a756-6f062820867e.png "Polycom VVX-401")

The Polycom VVX-4xx/5xx Phone Series are 12-line IP Phones with Color Display, which is a full-featured VoIP (Voice over Internet Protocol) phone that provide voice communication over an IP network. It provides traditional features, such as call forwarding, redialing, speed dialing, transferring calls, conference calling, and accessing voice mail. Calls can be made or received with a handset, headset, or speaker.

The Polycom VVX-4xx/5xx Series IP Phones provides a web interface (aka: GUI - Graphical User Interface) for the phone user that allows you to configure some features of your phone by using a web browser.

This article will guide you through the steps for basic configuration to make it work with HOIP.

!!! note "These steps MIGHT work with other Polycom Models. The examples below are to give guidance in your attempts to provision/configure your Polycom Models.  Images and screenshots in this article refer to the VVX-401."

## Factory Reset - (if required)

??? info "This is an optional step, which will completely wipe the phone"

    The below steps are an option to be considered, if one the following is observed:

    * The phone is on a boot loop and no longer going to the home menu
    * The default password or mac password doesn't work
    * If it's a 3rd party phone

    To factory-reset your device, carry out the following steps

    1. Reboot the phone and wait for the starting application.
    2. While the phone is in the starting application wait for the cancel button to appear then press it.
    3. The phone will show a 7 seconds count down. This is the only open window to press the key combination to go to the hard reset page.

        !!! note "If the phone model is a"

            * VVX series (VVX300, 301, 310, 311, etc): Press and hold 1 3 5 within the 7-second count down until it prompts you to the password page
            * Sound Point IP 335: Press and hold 1 3 5 7 within the 7-second count down until it prompts you to the password page
            * Sound Point IP series (IP550,560,570, etc): Press and hold 4 6 8 and \* within the 7-second count down until it prompts you to the password page
            * Conference Phone IP5000, 6000, 7000: Press and hold 1 3 5 7 within the 7-second count down until it prompts you to the password page

    4. Enter the device's MAC ID as the password (e.g 0004f28619dc).
    5. Press the 2nd soft key that corresponds to the mode or (encoding) to change it to `A->abc` or `a->abc`.
    6. Then (for example) to select the letter F, press the 3 key three times.

## Step 1 - Get the IP address of your phone

1. Press the `Home` Button Icon on your Polycom Phone.

      ![PolyVVX-401_Phone_Home_Button "A picture of the home button on the Polycom VVX-401"](https://user-images.githubusercontent.com/40501228/186971150-ee8cd2a8-53bd-4c19-9a24-8cf453cdea6f.png "A picture of the home button on the Polycom VVX-401")

2. On the `Display Screen` and using the `Arrow Keys` to scroll and select `Settings`.
3. Scroll down to `Status` and hit `Select`.
4. Scroll down to `Network` and hit `Select`.
5. Scroll down to `TCP/IP Parameters` and hit `Select`.

This should show your IP Address in the format of xxx.xxx.xxx.xxx (EX: 192.168.0.2)

## Step 2 - Logging in to the Phone Web User Interface

1. On your PC, open a Web browser window. (Note: Your PC must be on the same network as the phone.)
2. Enter the IP address in the browser address bar.
   This is the IP address you obtained above
   ***note: if the IP address does not resolve, use https://xxx.xxx.xxx.xxx, if that does not resolve, use http://xxx.xxx.xxx.xxx. Some web portals will not resolve without https/http being defined in the ip address.

You will now see this screen (see picture):

![PolyVVX-4xx_Admin_Login](https://user-images.githubusercontent.com/40501228/186971274-1e9c79e5-9db8-4f34-837b-496b0035f08a.png)

## Step 3 - Configure "Simple Setup" Fields

After successful login of User ADMIN, click on  `Simple Setup` button near the top left side of the screen. You will then need to populate only the `Header Fields`  as the pictured in the below example.

![PolyVVX-4xx_Simple_Setup](https://user-images.githubusercontent.com/40501228/186971309-fc32d13e-798a-418b-93fa-eb94ba2f5eab.png)

As the example pictured above, enter your information into the following fields:

| **TIME SYNCHRONIZATION** ||
| -- | -- |
| Alternate SNTP Server: | north-america.pool.ntp.org |
| Alternate Time Zone: | (your timezone) |
| **SIP SERVER** ||
| Address: | This will be the domain name sent in your credentials email<br />(ex: `pbx-us1.hamsoverip.com`) |
| Port: | 5160 |
| **SIP OUTBOUND PROXY** ||
| Address: | This will be the domain name sent in your credentials email<br />(ex: `pbx-us1.hamsoverip.com`) |
| Port: | 5160 |
| **SIP LINE IDENTIFICATION** ||
| Display Name: | How you want your "Caller ID" to be displayed to the Called Party. |
| Address: | Enter your **Extension** from the credentials email. |
| Authentication User ID: | Enter your Extension from the credentials email. |
| Authentication Password: | Enter your password from the credentials email. |
| Label: | Your choice on how you want to label your "Line Key" on your phone display |

Select `SAVE` before leaving screen.

If phone reboots, log back in as user ADMIN and continue to Step 4

## Step 4 - Configure "SIP" Fields

After completing Step 3, click on  `Settings` button near the top left side of the screen and choose `SIP`. You will then only need to populater the `SIP Fields` as the pictured in the below example.

![PolyVVX-4xx_SIP_Settings_UDPOnly](https://user-images.githubusercontent.com/40501228/186977655-6c78bd46-d138-4374-8512-de3044bde942.png)

As the example pictured above, enter your information into the following fields:

| **OUTBOUND PROXY** ||
| -- | -- |
| Address: | This will be the domain name sent in your credentials email<br />(ex: `pbx-us1.hamsoverip.com`) |
| Port: | 5160 |
| Transport: | UDPOnly |
| **SERVER 1** ||
| Special Interop: | Standard |
| Address: | This will be the domain name sent in your credentials email<br />(ex: `pbx-us1.hamsoverip.com`) |
| Port: | 5160 |
| Transport: | UDPOnly |
| Expires (s): | 3600 |
| Subscription Expires (s): | 3600 |
| Register (Radio Button): | Yes |
| Retry Timeout (ms): | 0 |
| Retry Maximum Count: | 3 |
| Line Seize Timeout (s): | 30 |

Select `SAVE` before leaving screen.

If phone reboots, log back in as user ADMIN and continue to Step 5

## Step 5 - Configure "LINE" Field

After completing Step 4, click on  `Settings` button near the top left side of the screen and then choose `LINES` and highlight `Line 1`.
Then you will population the only the `Line 1`  as the pictured in the below example.

![PolyVVX-4xx_Line_Settings_UDPOnly](https://user-images.githubusercontent.com/40501228/186977709-adbf52a8-fa45-4eb9-91ee-c887caeb55c0.png)

As the example pictured above, enter your information into the following fields:

| **IDENTIFICATION** ||
| -- | -- |
| Display Name: | (your choice)<br />(This is the name YOU will see on your Phone Display for Line 1) |
| Address: | Enter your **Extension** from the credentials email. |
| Label: | (your choice)<br />Recommend using the same entry from `Display Name` above. |
| Type (Radio Button): | Private |
| Third Party Name: | (leave blank) |
| Number of Line Keys: | 1 |
| Calls Per Line: | Default is "24" - Enter at least "1" |
| Enable SRTP (Radio Button): | No |
| Offer SRTP (Radio Button): | No |
| Require SRTP (Radio Button): | No |
| Server Auto Discovery: | Disable |
| **AUTHENTICATION** ||
| Use Login Credentials (Radio Button): | Enable |
| Domain: | This will be the domain name sent in your credentials email<br />(ex: `pbx-us1.hamsoverip.com`) |
| User ID: | Enter your Extension from the credentials email. |
| Password: | Enter your password from the credentials email. |
| **OUTBOUND PROXY** ||
| Address: | This will be the domain name sent in your credentials email<br />(ex: `pbx-us1.hamsoverip.com`) |
| Port: | 5160 |
| Transport: | UDPOnly |
| **SERVER 1** ||
| Special Interop: | Standard |
| Address: | This will be the domain name sent in your credentials email<br /> (ex: `pbx-us1.hamsoverip.com`) |
| Port: | 5160 |
| Transport: | UDPOnly |
| Expires (s): | 3600 |
| Subscription Expires (s): | 3600 |
| Register (Radio Button): | Yes |
| Retry Timeout (ms): | 0 |
| Retry Maximum Count: | 3 |
| Line Seize Timeout (s): | 30 |

Select `SAVE` before leaving screen.

Now with Steps 3 thru 5 provisioned/configured, reboot the phone to bind the changes/additions.

---

!!! info "Written 2022-08-28 by Mark KI5CYA, last updated 2024-08-13 by Dave M7TLB, note added 2025-07-19 by Jake W4EWO"
