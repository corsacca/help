---
layout: article
title: Import Data to your Vault
categories: [import-export]
featured: true
popular: true
tags: [import]
order: 01
---

Bitwarden provides a data import tool for easy migration from any password management solution to your personal Vault or Organization Vault (see [Import Data to an Organization]({% link _articles/organizations/import-to-org.md %})).

You can also use the data import tool to import from one Bitwarden Vault to another, or to import a backup [Encrypted Export]({% link _articles/importing/encrypted-export.md %}).

Bitwarden supports a large array of formats for import, including those used by the most popular password management solutions:

- [Import from LastPass]({% link _articles/importing/import-from-lastpass.md %})
- [Import from 1Password]({% link _articles/importing/import-from-1password.md %})
- [Import from Firefox]({% link _articles/importing/import-from-firefox.md %})
- [Import from Google Chrome]({% link _articles/importing/import-from-chrome.md %})

For a full list of supported formats, see [Supported Formats](#supported-formats).

## Import to your Personal Vault

To import your data into a personal Vault:

1. Log in to the [Web Vault](https://vault.bitwarden.com){:target="\_blank"}.
2. Select **Tools** from the top navigation bar.
3. Select **Import Data** from the left Tools menu.
4. Select the format of your file to import from the dropdown menu.

   {% callout success%}If you're importing an [Encrypted Export]({% link _articles/importing/encrypted-export.md %}), select `.json` as you would if it were plaintext. A handler will determine that the file is encrypted and decrypt using your [account encryption key](https://bitwarden.com/help/article//change-your-master-password/#rotating-your-accounts-encryption-key).{% endcallout %}
5. Select the **Browse** button and add your file.
6. Select the **Import Data** button to complete your import.

{% callout warning %}
Importing data multiple times will create duplicates.
{% endcallout %}

## Troubleshooting Import Errors

If you get the following error:

```
Ciphers[X].Login: The field yyyy exceeds the maximum encrypted value length of zzzz characters.
```

An item in your `.csv` exceeds the character limit allowed for items stored in the Bitwarden Vault. Remove the offending item from your file for import, or reduce its size. Open the `.csv` in a text editor or spreadsheet program for easy editing, and locate the offending item at `index[X]` as referenced in the error message.

{% callout info %}
Depending on the program you use to edit your `.csv`, the index value `[X]` may not map perfectly to a Row or Line number. Typically in spreadsheet programs, add 2 (i.e. `index[23]` = Row **25**). In other cases, it may be useful to focus on `Notes` items, as these items are usually those that trigger the error.
{% endcallout %}

## Supported Formats

The following formats are supported out-of-the-box:

{% callout info %}
If your format is not listed below, manually [condition a Bitwarden .csv or .json]({% link _articles/importing/condition-bitwarden-import.md %}).
{% endcallout %}

- [1Password (1pif)]({% link _articles/importing/import-from-1password.md %})
- [1Password 6 &amp; 7 Windows (.sv)]({% link _articles/importing/import-from-1password.md %})
- [1Password 6 &amp; 7 Mac (csv)]({% link _articles/importing/import-from-1password.md %})
- Ascendo DataVault (csv)
- Avast Passwords (csv)
- Avira (json)
- BlackBerry Password Keeper (csv)
- Blur (csv)
- [Brave (csv)]({% link _articles/importing/import-from-chrome.md %})
- [Chrome (csv)]({% link _articles/importing/import-from-chrome.md %})
- Clipperz (html)
- Codebook (csv)
- Dashlane (json)
- Encryptr (csv)
- Enpass (csv)
- Enpass (json)
- [Firefox (csv)]({% link _articles/importing/import-from-firefox.md %})
- F-Secure KEY (fsk)
- GNOME Passwords and Keys/Seahorse (json)
- Kaspersky Password Manager (txt)
- KeePass 2 (xml)
- KeePassX (csv)
- Keeper (csv)
- [LastPass (csv)]({% link _articles/importing/import-from-lastpass.md %})
- LogMeOnce (csv)
- Meldium (csv)
- mSecure (csv)
- Myki (csv)
- [Microsoft Edge (Chromium) (csv)]({% link _articles/importing/import-from-chrome.md %})
- [Opera (csv)]({% link _articles/importing/import-from-chrome.md %})
- Padlock (csv)
- Passbolt (csv)
- PassKeep (csv)
- Passman (json)
- Passpack (csv)
- Password Agent (csv)
- Password Boss (json)
- Password Dragon (xml)
- Password Safe (xml)
- PasswordWallet (txt)
- RememBear (csv)
- RoboForm (csv)
- SafeInCloud (xml)
- SaferPass (csv)
- SecureSafe (csv)
- SplashID (csv)
- Sticky Password (xml)
- True Key (csv)
- Universal Password Manager (csv)
- [Vivaldi (csv)]({% link _articles/importing/import-from-chrome.md %})
- Yoti (csv)
- Zoho Vault (csv)
