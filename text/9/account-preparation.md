---
title: Account Preparation
---

## Account Preparation

Full-time students at NCSU with active Unity accounts are allocated space on the AFS servers from which to host a small website, if they so desire. In order to take advantage of this offering, you must manually configure your account and storage space first.

Understanding how your account should be set up is important. If you ever wanted to remove permissions so that your site could no longer be viewed by the public, take note below of what permissions are set and remove them.

### Manual Setup

1. Sign into your terminal.
2. Create a new directort directly inside your home directory with the name `www`.
3. Give the AFS user `www:servers` the look permission in your home directory.
4. Give the AFS user `www:servers` the read and look permissions in your newly created `www` directory.
5. Using your text editor and ExpanDrive, create a new file in your newly created `www` directory called `index.html`.
6. In your web browser, navigate to http://www4.ncsu.edu/~unityid/ (making sure to substitute your own unity id) and ensure there is no error message.
 * As you edit the `index.html` file, your changes will be reflected on this webpage.

```bash
mkdir ~/www
fs sa ~/ www:servers l
fs sa ~/www www:servers rl
```

If you want to perform maintenance on your webpage, you may desire to bring it “offline” temporarily. You can do so by temporary removing the permissions for the ‘www’ directory.

```bash
fs sa ~/www www:servers none
```

### Why is there an Error?

It is important to note that if there is not an `index.html` file in your `www` directory, you will see an error. Most likely one of the following errors: **The requested URL /~unityid/index.html was not found on this server.**, or a **403 Forbidden**.

To rectify this error, simply create a blank `index.html` page and save it to your `www` directory.

If you are looking for a file of a different name, simply type the URL http://www4.ncsu.edu/~unityid/name.html into your web browser.
