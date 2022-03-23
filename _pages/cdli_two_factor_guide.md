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

## 1) [If you have a smartphone (GAuth)](#setup-guide-for-smartphone-users)

## 2) [No smartphone: Chrome on a computer (GAuth plugin)](#setup-guide-for-google-chrome-users)
<br/>
<br/>

# Setup Guide for Smartphone Users
if you do not have access to a **smartphone** and are a **Google Chrome** user, [Click Here](#setup-guide-for-google-chrome-users)
### Pre Requirements : 

1. Download **Google Authenticator** application on your device.

    - For Android devices, Playstore Link : [Google Authenticator](https://play.google.com/store/apps/details?id=com.google.android.apps.authenticator2)

    - For IOS devices, Appstore Link : [Google Authenticator](https://apps.apple.com/in/app/google-authenticator/id388497605) 

    - Google Help answer : [Install Google Authenticator](https://support.google.com/accounts/answer/1066447)

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

<br/>
<br/>

# Setup Guide for Google Chrome Users
This guide is intended towards people with no access to smartphone. If you have a smartphone, please follow the [instructions for smartphone users](#setup-guide-for-smartphone-users). This Guide will walk you through the steps required to setup the **GAuth Authenticator in Google Chrome**. By the end of this guide, you will be able to use **2FA** authentication to login to **OUR WEBSITE**.
#### Install GAuth Authenticator :
GAuth Authenticator can be found and downloaded from the **Chrome Store**, simply visit- https://chrome.google.com/webstore/detail/gauth-authenticator/ilgcnhelpchnceeipipijaljkblbcobl

#### Adding the extension to chrome browser :
Click on the **Add to Chrome** button located on the right. A pop-up appears on the screen asking for your confirmation to add the extension to your chrome browser.
![Screenshot-12.jpg](/assets/image/Screenshot-12.jpg)

#### Enabling extension :
1) To enable the extension, click on the **manage extensions** icon on the toolbar and search for **GAuth Authenticator**.
2) Click on the three vertical dots present at the immediate right of our extension.
3) (optional) You can pin the extension to the quickaccess toolbar for easier access by clicking on the **pin** icon.
![Screenshot-13.jpg](/assets/image/Screenshot-13.jpg)

#### Login to your account for any desired website :
You can login to an existing account or create a new one.

#### Now it's time to set up our two factor authenticator (2FA) :
1) Once you successfully login to the website, browse to my **account/ manage account > settings> security** and scroll down to find two Factor Authentication (2FA).
![Screenshot-14.jpg](/assets/image/Screenshot-14.jpg)
2) Follow the instructions mentioned to setup **2FA**.
3) Once the above steps are done and you enable 2FA, another pop up window appears displaying a **MANUAL KEY** which is a random combination of letters and numbers. Copy the MANUAL KEY.
![Screenshot-15.jpg](/assets/image/Screenshot-15.jpg)
4) Browse back to your GAuth Authenticator and click on the **edit** icon on the top right corner of the window.
5) Click on **"+Add"** button present under the **One-time passwords** bar. This allows you to add and setup mutliple 2FA for multiple websites and manage it in a single space.
![Screenshot-16.jpg](/assets/image/Screenshot-16.jpg)
6) Set the **Account Name** to your desired choice. eg- ("Gitlab" for gitlab login).
7) Now paste the MANUAL KEY that we copied earlier and paste it in the **Secret Key** tab. simply click on the **"+Add"** button below to complete the process.
![Screenshot-17.jpg](/assets/image/Screenshot-17.jpg)

Do this for any number of websites you want. You can manage all of these One-time passwords from a single space which makes it very convenient to use. keep in mind the **timer** on the top right side. It tells you the remaining time you have, to enter the 2FA password before it expires and asks you to enter another newly generated password!
![Screenshot-18.jpg](/assets/image/Screenshot-18.jpg)
##### You have successfully added 2FA and extra security to your favourite website!
