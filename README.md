# Cloudflare Office 365 setup CLI

Very basic commands to verify and setup DNS records in Cloudflare to match an Office 365 email domain

## Installation

``` $ npm install ```

## Usage

```
  $ export CF_USERNAME="yourcloudflare@email.com"
  $ export CF_API_KEY="yourApiKey"
  $ npm run <action> -- <domain> [extra]
```

## Actions

For all actions, you can refer to [the Office 365 DNS records](./blob/master/office365/index.js)

### verify

``` $ npm run verify -- <domain> <mscode> ```

The mscode is the value given during the "Verify" phase when adding a new domain on office365:

![verify code on office365](https://cloud.githubusercontent.com/assets/487758/20955500/a89ef25c-bc7e-11e6-8d22-2bacd29527b0.png)

### setup

``` $ npm run setup -- <domain> ```

This will set up 2 SRV, 5 CNAME, 1 MX and 1 TXT entry

# Contribute

At the moment, this is used internally at [Red Ape Solutions](https://redapesolutions.com).  
Therefore there are probably many cases we are not taking into consideration.

Feel free to [submit issues](https://github.com/redapesolutions/cloudflare-office365-setup/issues) or even better, [pull requests](https://github.com/redapesolutions/cloudflare-office365-setup/pulls)

When committing, please use `npm run commit` 
