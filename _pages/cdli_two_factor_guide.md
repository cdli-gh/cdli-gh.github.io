---
title: "Two Factor Guide"
permalink: /guides/cdli_two_factor_guide.html
sidebar:
  nav: "guides"
toc: true
---

# Two Factor Authentication (2FA)

Two-factor Authentication (2FA), sometimes referred to as two-step verification or dual-factor authentication, is a security process in which users provide two different authentication factors to verify themselves. This process is done to better protect both the user's credentials and the resources the user can access. 

Two-factor authentication provides a higher level of security than authentication methods that depend on single-factor authentication (SFA), in which the user provides only one factor -- typically, a password or passcode. Two-factor authentication methods rely on a user providing a password, as well as a second factor, usually either a security token or a biometric factor, such as a fingerprint or facial scan.

## How to set up Two Factor for CDLI?

### Pre Requirements : 

1. Download **Google Authenticator** application on your device.

    For Android devices, Playstore Link : [Google Authenticator](https://play.google.com/store/apps/details?id=com.google.android.apps.authenticator2)

    For IOS devices, Appstore Link : [Google Authenticator](https://apps.apple.com/in/app/google-authenticator/id388497605) 

    Google Help answer : [Install Google Authenticator](https://support.google.com/accounts/answer/1066447)

### Steps :

*NOTE :* **Setup 2FA** or **Verify 2FA** have to be completed within **2:30 minutes or 150 seconds**. 

#### To set up 2FA :

User will be prompted to set up 2FA when the user registers or when a user requests to change the 2FA (future enhancements).

1. After the user submits the registration form, the user will be prompted to set up 2FA (as shown below)

    ![Two Factor Authentication Setup](/assets/image/Two_Factor_Authentication_Setup.png)

    From the above image,

    **1** : Secret Code

    **2** : Secret Key (**IMPORTANT !!**)

    **3** : QR Code based on Secret Key

2. User will have to store the **Secret Key** safely as this key will help to retrieve the 2FA code.

3. After backing up code successfully, its time to set up 2FA on **Google Authenticator** App. 

    **Google Authenticator** provides 2 ways to set up 2FA : 

    a. *Scan a QR Code*  option
    
        Scan the QR code (shown in Step 1)
    
    **OR**
    
    b. *Manual Mode* or *Enter a setup key* option
    
        Enter Account name  : **Enter a suitable name. ex. CDLI** 
        Your key            : **Your Secret Key (shown in Step 1)** 
        Type of key         : Timer Based

4. Now on 2FA setup page, enter the **Code** as **Checking code** (shown in Step 1) and then verify if you have backed up **Secret key** and select the checkbox "*I have backed up my 16-digit key*". 

5. Click on **Enable 2FA** button to complete the 2FA setup process.

#### To verify 2FA :

User will be prompted to verify 2FA when the user tries to log in or when setting a new password using Forgot Password functionality.
 
User has to be ready with code generated on Google Authenticator. 

1. On submitting the login form, the user will be prompted to 2FA verification (as shown below).

    ![Two Factor Authentication Setup](/assets/image/Two_Factor_Authentication_Verify.png)

2. Enter the code generated on **Google Authenticator** (as shown below)

    ![Two Factor Authentication Setup](/assets/image/Two_Factor_Authentication_Code.png)  
    Do not add a space in the code, input all 6 didgits one after another.

3. Click **Submit** to complete the verification.
