# Make your own ClientID - This works!

{% hint style="info" %}
This is a bit of an involved process, but don't worry, it's doable.

I've made this guide because I had to piece some steps together from a few other sources.

There was also a step that nobody mentioned, which I had to realise for myself.

Hand-holding is exactly how I learned to use & configure & fix Linux, so I shall do the same for you — there's no shame in this, despite how loudly half the Linux community will shout you down when you ask for help.
{% endhint %}

#### Sources

* [RClone.org — Making your own client ID](https://rclone.org/drive/#making-your-own-client-id)&#x20;

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

<figure><img src="../../.gitbook/assets/image.png" alt="" width="518"><figcaption></figcaption></figure>

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

<figure><img src="../../.gitbook/assets/image (2).png" alt=""><figcaption></figcaption></figure>

If you have more than one Google Cloud project, double-check at the top of the page that you are in the right project! It's a button next to the Google Cloud heading:

<figure><img src="../../.gitbook/assets/image (7).png" alt=""><figcaption></figcaption></figure>

Then click the blue "Enable button":

<figure><img src="../../.gitbook/assets/image (6).png" alt="" width="491"><figcaption></figcaption></figure>


{% endstep %}

{% step %}
### Create the OAuth Consent Screen

Go to the OAuth Consent Screen in the sidebar menu, or click this button:

<a href="https://console.cloud.google.com/auth/overview" class="button primary">OAuth Management</a>

Click the <kbd><mark style="color:blue;">Get started<mark style="color:blue;"></kbd> button:

<figure><img src="../../.gitbook/assets/image (8).png" alt="" width="467"><figcaption></figcaption></figure>

a) **App Information**

Type a name for the app. This doesn't really matter because only you are going to see this, when you log in to your Google account through KDE.

<figure><img src="../../.gitbook/assets/image (9).png" alt=""><figcaption></figcaption></figure>

Add your email address by just clicking in the box. You can only choose your address.

Click <kbd><mark style="color:blue;">Next<mark style="color:blue;"></kbd>.

b) **Audience**

Choose _Internal_ or _External_.&#x20;

I don't think this matters too much, because _Internal_ means that only you (and your organisation, if you have Google Workspace) can access it; and _External_ means that people can only use it if you've added them to the list of test users. Others won't be able to use it unless you have "verified" your app, which is _hard_ so no worries there. Regardless, even if others can use it, they'll still only be connecting to _**their**_ Google account.

<figure><img src="../../.gitbook/assets/image (10).png" alt="" width="515"><figcaption></figcaption></figure>

c) **Contact Information**

Just add your email address here.

<figure><img src="../../.gitbook/assets/image (11).png" alt="" width="530"><figcaption></figcaption></figure>

d) **Finish and Create**

Check the "I agree" box, click <kbd><mark style="color:blue;">Continue<mark style="color:blue;"></kbd>, then click <kbd><mark style="color:blue;">Create<mark style="color:blue;"></kbd>.

<figure><img src="../../.gitbook/assets/image (12).png" alt=""><figcaption></figcaption></figure>


{% endstep %}

{% step %}
### Data Access — add scopes

Click **Data access** in the sidebar or click this button:

<a href="https://console.cloud.google.com/auth/scopes" class="button primary">Data access</a>

_Remember to check that you're in the right project if you have more than one._

Now you have to add "scopes" — these are aspects of the data in your Google account that you want to access. For security, the Google Cloud API only allows access to the aspects of your data that have been explicitly defined and requested.

<figure><img src="../../.gitbook/assets/image (13).png" alt=""><figcaption></figcaption></figure>


{% endstep %}
{% endstepper %}

[^1]: idk = "I don't know"
