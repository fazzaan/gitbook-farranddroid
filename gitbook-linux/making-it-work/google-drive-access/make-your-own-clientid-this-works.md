# Make your own ClientID - This works!

{% hint style="info" %}
This is a bit of an involved process, but don't worry, it's doable.

I've made this guide because I had to piece some steps together from a few other sources.

There was also a step that nobody mentioned, which I had to realise for myself.

Hand-holding is exactly how I learned to use & configure & fix Linux, so I shall do the same for you — there's no shame in this, despite how loudly half the Linux community will shout you down when you ask for help.
{% endhint %}

{% hint style="danger" %}
## THIS IS FOR KDE and RCLONE ONLY

In my experience so far, KDE is the only shell that is incapable of connecting to Google Drive. This isn't really the KDE dev team's fault. The guide I've written here is based on the guide that RClone gave for connecting RClone to Google Drive using your own ClientID.

You _**can**_ use this for other desktop shells and sync apps, but I haven't tried and have no idea how they work.
{% endhint %}

#### Sources

* [RClone.org — Making your own client ID](https://rclone.org/drive/#making-your-own-client-id) — main useful guide
* [KDE Online Accounts - Not Signing In](https://discuss.kde.org/t/kde-online-accounts-not-signing-in/3411/1) — chatty discussion about the bug, mostly unhelpful but could help you to understand the issue better
*

## Steps

{% stepper %}
{% step %}
### If you've already tried to log in to your Google account in KDE, delete the account from the Online Accounts.

We're going to modify the connection parameters, so you'll need to connect your account afresh.

Moreover, it appears that KDE's Online Accounts only allows for one Google account connection, which seems a bit odd but whatever.


{% endstep %}

{% step %}
### Log in to the Google API Console

Here: [https://console.developers.google.com/](https://console.developers.google.com/)&#x20;

Any account is fine, doesn't need to be the same one as the Drive account you want to access.


{% endstep %}

{% step %}
### Create a new project

Call it whatever you like.

Don't worry about the "no organisation" bit.

<figure><img src="../../.gitbook/assets/image (5) (1).png" alt="" width="518"><figcaption></figcaption></figure>

Click <kbd><mark style="color:blue;">Create<mark style="color:blue;"></kbd>.


{% endstep %}

{% step %}
### Go to the APIs & Services dashboard

Idk[^1] why but the APIs link wasn't visible anywhere.

Click here to go to the dashboard: [https://console.cloud.google.com/apis/dashboard](https://console.cloud.google.com/apis/dashboard)&#x20;

Then click "Enable APIs and services" at the top,

**OR click here to go directly to the API Library:**&#x20;

<a href="https://console.cloud.google.com/apis/library" class="button primary">Google Cloud API Library</a>


{% endstep %}

{% step %}
### Enable the Google Drive API

Scroll down to find it, you should see this. Click it.

<figure><img src="../../.gitbook/assets/image (2) (1) (1).png" alt=""><figcaption></figcaption></figure>

If you have more than one Google Cloud project, double-check at the top of the page that you are in the right project! It's a button next to the Google Cloud heading:

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/image (7).png" alt=""><figcaption></figcaption></figure></div>

Then click the blue "Enable button":

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/image (6) (1).png" alt="" width="491"><figcaption></figcaption></figure></div>


{% endstep %}

{% step %}
### Create the OAuth Consent Screen

Go to the OAuth Consent Screen in the sidebar menu, or click this button:

<a href="https://console.cloud.google.com/auth/overview" class="button primary">OAuth Management</a>

Click the <kbd><mark style="color:blue;">Get started<mark style="color:blue;"></kbd> button:

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/image (8).png" alt="" width="467"><figcaption></figcaption></figure></div>

a) **App Information**

Type a name for the app. This doesn't really matter because only you are going to see this, when you log in to your Google account through KDE.

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/image (9).png" alt=""><figcaption></figcaption></figure></div>

Add your email address by just clicking in the box. You can only choose your address.

Click <kbd><mark style="color:blue;">Next<mark style="color:blue;"></kbd>.

b) **Audience**

Choose _Internal_ or _External_.&#x20;

I don't think this matters too much, because _Internal_ means that only you (and your organisation, if you have Google Workspace) can access it; and _External_ means that people can only use it if you've added them to the list of test users. Others won't be able to use it unless you have "verified" your app, which is _hard_ so no worries there. Regardless, even if others can use it, they'll still only be connecting to _**their**_ Google account.

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/image (10).png" alt="" width="515"><figcaption></figcaption></figure></div>

{% hint style="info" %}
## NOTE

"Internal" is the better choice as long as the Google Drive you want to connect to is part of the same Google Workspace as this Cloud project. If you are an individual Google account user then this is fine.

"External" will require you to either:

a) publish the project, which is a lengthy, complicated and arduous process, with a bunch of verification hoops, awaiting a Google employee to verify your project;

b) keep the project in "testing" mode, which will expire after 1 week so you'll have to keep logging in to your Google account in KDE once a week.

#### Choose **Internal**.
{% endhint %}

​c) **Contact Information**

Just add your email address here.

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/image (11).png" alt="" width="530"><figcaption></figcaption></figure></div>

d) **Finish and Create**

Check the "I agree" box, click <kbd><mark style="color:blue;">Continue<mark style="color:blue;"></kbd>, then click <kbd><mark style="color:blue;">Create<mark style="color:blue;"></kbd>.

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/image (12).png" alt="" width="411"><figcaption></figcaption></figure></div>


{% endstep %}

{% step %}
### Data Access — add scopes

Click **Data access** in the sidebar or click this button:

<a href="https://console.cloud.google.com/auth/scopes" class="button primary">Data access</a>

_Remember to check that you're in the right project if you have more than one._

Now you have to add "scopes" — these are aspects of the data in your Google account that you want to access. For security, the Google Cloud API only allows access to the aspects of your data that have been explicitly defined and requested.

Click the <kbd><mark style="color:blue;">**Add or remove scopes**<mark style="color:blue;"></kbd> button.

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/image (1) (1).png" alt="" width="500"><figcaption></figcaption></figure></div>

There are around 250 available scopes in this list, so do use the Filter at the top of the table if necessary.&#x20;

{% hint style="info" %}
Note that typing something into the filter box does not select the scope that appears! The behaviour of the filter is a bit strange. After pressing Enter in the search filter, you also have to tick[^2] the checkboxes next to each scope that you need.
{% endhint %}

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/image (2) (1).png" alt=""><figcaption></figcaption></figure></div>

In this filter box, search for each of these scope names:

* userinfo.email
* userinfo.profile
* docs
* drive
* drive.metadata.readonly

You may add more if you think they are necessary.

{% hint style="info" %}
The default `/usr/share/accounts/providers/kde/`<mark style="color:green;">**`google.provider`**</mark> file also contains the scopes `calendar`, `tasks`, `youtube.upload` and `m8/feeds`. It seems that these work automatically and don't need to be added in our custom Google Cloud project.
{% endhint %}

**CLICK THE BLUE&#x20;**<kbd><mark style="color:blue;">**UPDATE**<mark style="color:blue;"></kbd>**&#x20;BUTTON!!!**

For some reason it is possible to click outside of the popup scope panel and it will close automatically, losing all the changes that you made. So click that <kbd><mark style="color:blue;">**UPDATE**<mark style="color:blue;"></kbd> button!

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/image (3) (1).png" alt=""><figcaption></figcaption></figure></div>

Finally click the blue <kbd><mark style="color:blue;">**Save**<mark style="color:blue;"></kbd> button.

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/image (4) (1).png" alt="" width="503"><figcaption></figcaption></figure></div>


{% endstep %}

{% step %}
### Add yourself as a user

Click **Audience** in the sidebar, or click this button:

<a href="https://console.cloud.google.com/auth/audience" class="button primary">Audience</a>

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/image (15).png" alt="" width="243"><figcaption></figcaption></figure></div>

Scroll down to Test users and click <kbd><mark style="color:blue;">**+ Add users**<mark style="color:blue;"></kbd>.

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/image (17).png" alt=""><figcaption></figcaption></figure></div>

Add your Google account email address (the one that you type when you sign in to your Google account) and click <kbd><mark style="color:blue;">**Save**<mark style="color:blue;"></kbd>.

Only Google accounts listed in here will be able to sign in using the ClientID that we're creating.


{% endstep %}

{% step %}
### Create OAuth client

Go to the **Overview** in the sidebar, then click <kbd>**Create OAuth client**</kbd> in the **Metrics** section; or click this button to go there directly:

<a href="https://console.cloud.google.com/auth/clients/create" class="button primary">Create OAuth client</a>

Choose **Desktop app** as application type, and give it a name (or keep the default, it doesn't matter — this is only for you to identify it in your Cloud projects console).

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/image (18).png" alt="" width="521"><figcaption></figcaption></figure></div>

A panel will appear, THIS IS VERY IMPORTANT!

"OAuth client created"

Here, you _**must**_ <kbd><mark style="color:blue;">**Download JSON**<mark style="color:blue;"></kbd> to save your Client ID and Client Secret because if you don't, you will not be able to access your Client Secret again!!! (However, I actually was able to. But Google are liable to change anything at any time so download it!)

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/image (19).png" alt="" width="491"><figcaption></figcaption></figure></div>

After download the JSON file and saving it somewhere safe, copy and paste the ID and the Secret somewhere handy because you're about to use these in a configuration file on your computer.


{% endstep %}

{% step %}
### Back up your Google.Provider file

{% hint style="danger" %}
## HERE BE DRAGONS

But only there be dragons if you don't make backups of the files we edit, so

simple solution:

make backups.
{% endhint %}

Go to `/usr/share/accounts/providers/` in your file browser. I recommend **Dolphin** because it handles root/superuser access like a boss, instead of the class clown Gnome Files.

```
/usr/share/accounts/providers/
```

Right click on the `kde` folder and click "open as adminstrator".

_(You can also just press_ <kbd>Ctrl</kbd>+<kbd>Alt</kbd>+<kbd>Shift</kbd>+<kbd>A</kbd> _to switch to adminstrator mode!)_

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/image (21).png" alt="" width="274"><figcaption></figcaption></figure></div>

Inside the **`kde`** folder, right click on the file `google.provider` and choose <kbd>Duplicate here</kbd>, or press <kbd>**Ctrl**</kbd>+<kbd>**D**</kbd>.&#x20;

<figure><img src="../../.gitbook/assets/image (22).png" alt=""><figcaption></figcaption></figure>

Rename the backup version to whatever you want so that you remember what it is.

Now open the google.provider file in a text editor. Or you can do all this through command line, but there's a lot of copying and pasting of messy strings of characters so I prefer a GUI.

I recommend Kate text editor because, again, it actually handles root/superuser requests properly, unlike the Gnome counterpart.

{% hint style="info" %}
## POTENTIALLY OUTDATED

I wrote this guide in October 2025, so proceed from here with caution.

There are two ways you can go:

1. Copy and paste the whole file, and add your client ID and secret.
2. Edit the file contents manually.

Option 2 is better if you are reading this from the distant future. (In the Linux world, things change very fast so that could be any time after October 2025 🙃).
{% endhint %}


{% endstep %}

{% step %}
### Put the ClientID into your system

## Option 1: Copy and paste the whole file

```xml
<?xml version="1.0" encoding="UTF-8"?>
<provider id="google">
  <name>Google</name>

  <description>NAME configured this - Sync calendars, contacts, and tasks, and upload videos to YouTube in supported apps</description>
  <icon>im-google</icon>
  <translations>kaccounts-providers</translations>
  <domains>.*google\.com</domains>

  <template>
    <group name="auth">
      <setting name="method">oauth2</setting>
      <setting name="mechanism">web_server</setting>
      <group name="oauth2">
        <group name="web_server">
          <setting name="Host">accounts.google.com</setting>
          <setting name="AuthPath">o/oauth2/auth?access_type=offline&amp;approval_prompt=force</setting>
          <setting name="TokenPath">o/oauth2/token</setting>
          <setting name="RedirectUri">http://localhost/oauth2callback</setting>

          <setting name="ResponseType">code</setting>
          <setting type="as" name="Scope">[
            'https://www.googleapis.com/auth/userinfo.email',
            'https://www.googleapis.com/auth/userinfo.profile',
            'https://www.googleapis.com/auth/calendar',
            'https://www.googleapis.com/auth/tasks',
            'https://www.google.com/m8/feeds/',
            'https://www.googleapis.com/auth/youtube.upload',
            'https://www.googleapis.com/auth/docs',
            'https://www.googleapis.com/auth/drive',
            'https://www.googleapis.com/auth/drive.metadata.readonly'
            ]</setting>
          <setting type="as" name="AllowedSchemes">['https']</setting>
          <setting name="ClientId">CLIENT_ID_HERE</setting>
          <setting name="ClientSecret">CLIENT_SECRET_HERE</setting>
        </group>
      </group>
    </group>
  </template>
</provider>

```

**1.** Copy and paste the above block, and replace the following with your own:

* NAME = put your name here. This will appear in the Add Accounts panel when you add your Google account.
* CLIENT\_ID\_HERE = paste your Client ID. No quote marks around it.
* CLIENT\_SECRET\_HERE = paste your Client Secret. No quote marks around it.

**2.** Save the file.



## Option 2: Edit the file manually

**1.** In the section `<setting type="as" name="Scope">`, add the following URLs if they aren't already there:

* https://www.googleapis.com/auth/userinfo.email
* https://www.googleapis.com/auth/userinfo.profile
* https://www.googleapis.com/auth/docs
* https://www.googleapis.com/auth/drive
* https://www.googleapis.com/auth/drive.metadata.readonly

Ensure that each is wrapped with a quote mark `'` , and that every line is ended with a comma `,` except for the last line.

**2.** Replace the ClientID with yours in the tag `<setting name="ClientId">`.

**3.** Replace the Client Secret with yours in the tag `<setting name="ClientSecret">`.

**4.** Edit the \<description> tag so that you can see it in the Add accounts panel in KDE.

**5.** Save the file.


{% endstep %}

{% step %}
### Add your Google account to KDE's Online Accounts

The shortest route to do this is:

1. Open Dolphin
2. Click **Network** in the sidebar
3. Click **Google Drive** in the main panel
4. Click <kbd><mark style="color:blue;">**+ Add Account...**<mark style="color:blue;"></kbd> in the Online Accounts window that appears

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/image (23).png" alt="" width="396"><figcaption></figcaption></figure></div>

Choose your Google service from the list.

If you kept both `google.provider` files with the `.provider` file suffix, then both of them will show up in the add accounts list. You can see mine, I did the whole process a second time to ensure that I was writing the correct guidance for you:

<figure><img src="../../.gitbook/assets/image (24).png" alt="" width="523"><figcaption></figcaption></figure>

Here you will see the name of your app that you typed in [Step 6](make-your-own-clientid-this-works.md#create-the-oauth-consent-screen):

<figure><img src="../../.gitbook/assets/image.png" alt="" width="505"><figcaption></figcaption></figure>

Sign in, choose your account, etc.

If you opted for the "External" audience type, and you haven't had your app verified (of course you haven't, it's a crazy process), you will be greeted with this scary screen.&#x20;

Presumably you trust yourself, and you've been following along with this whole process, so you should understand that there aren't any risks here — you are simply connecting to your own Google account.

Click Advanced in the window, then click on the tiniest text, **"Go to&#x20;**_**APP NAME**_**&#x20;(unsafe)"**:

<figure><img src="../../.gitbook/assets/image (1).png" alt="" width="488"><figcaption></figcaption></figure>

You'll notice that this list is a list of the scopes that we added as scope URLs in the [Data Access section (Step 7)](make-your-own-clientid-this-works.md#data-access-add-scopes) and the `google.provider` file on your computer.

**Check the box next to Select all.**

<figure><img src="../../.gitbook/assets/image (2).png" alt="" width="484"><figcaption></figcaption></figure>
{% endstep %}
{% endstepper %}

So after all that, it ... doesn't work.

I don't know what happened.

I set it up the first time and it was fine, it worked perfectly.

Now it doesn't work at all, it doesn't even show any account connection settings in the KDE Online Accounts window, which it used to do, as did even the original google.provider version.&#x20;

It just shows this:

<figure><img src="../../.gitbook/assets/image (5).png" alt=""><figcaption></figcaption></figure>

So idk what happened.



And quite frankly, i'm tired of this shit

[^1]: idk = "I don't know"

[^2]: check the box
