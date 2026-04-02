# SSO

Configure Single Sign-On from **Settings → SSO Configuration** to let your team authenticate into Lema through your existing identity provider.

### Selecting an Identity Provider

Choose your IdP from the list to see provider-specific setup instructions and configuration fields:

* Okta
* Google Workspace
* Entra ID (Azure AD)
* JumpCloud
* PingOne
* OneLogin
* Salesforce
* PingFederate
* CyberArk

Selecting a provider loads a guided configuration flow tailored to that IdP's setup requirements.

### Direct Protocol Configuration

If your IdP isn't listed, you can configure SSO directly using a standard protocol:

* **SAML 2.0**
* **OIDC**

{% hint style="info" %}
SSO configuration requires Admin access. Contact your IdP administrator to obtain the metadata or credentials needed to complete the setup.
{% endhint %}
