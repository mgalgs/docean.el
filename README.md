## docean.el
*Interact with DigitalOcean from Emacs. -*- lexical-binding: t -*-*

---
[![License GPLv3](https://img.shields.io/badge/license-GPL_v3-green.svg)](http://www.gnu.org/licenses/gpl-3.0.html)
[![Build Status](https://travis-ci.org/emacs-pe/docean.el.svg?branch=master)](https://travis-ci.org/emacs-pe/docean.el)
[![MELPA](http://melpa.org/packages/docean-badge.svg)](http://melpa.org/#/docean)

> Note: `docean.el` uses the [API v2.0](https://developers.digitalocean.com/v2/) of DigitalOcean.

`docean.el` enables an easy interaction with DigitalOcean from
Emacs.

### Features

 + Show list of droplets.
 + Perform [droplet actions][].
 + Show actions performed by an account.

### Usage

To configure your account you need generate an api key in
https://cloud.digitalocean.com/settings/applications.  and to set
up, you can follow any of the following options:

 + Add `(setq docean-oauth-token "mytoken")` to your `init.el`
 + Set the environment variable `DO_API_TOKEN`.

To show your droplets you can use `M-x docean-droplet-list`.

### TODO

+ [ ] Handle `meta` abd `links` in API responses.

[droplet actions]: https://developers.digitalocean.com/#droplet-actions

### Function Documentation


#### `(docean-oauth-token)`

Return the configured DigitalOcean token.

#### `(docean-reboot-droplet ID)`

Reboot a droplet identified by ID.

#### `(docean-power-cicle-droplet ID)`

Power cicle a droplet identified by ID.

#### `(docean-shutdown-droplet ID)`

Shutdown a droplet identified by ID.

#### `(docean-power-off-droplet ID)`

Power off a droplet identified by ID.

#### `(docean-power-on-droplet ID)`

Reboot a droplet identified by ID.

#### `(docean-password-reset-droplet ID)`

Reset password a droplet identified by ID.

#### `(docean-enable-ipv6-droplet ID)`

Enable ipv6 to a droplet identified by ID.

#### `(docean-disable-backups-droplet ID)`

Disable backups a droplet identified by ID.

#### `(docean-enable-private-networking-droplet ID)`

Enable private networking a droplet identified by ID.

#### `(docean-rename-droplet ID &optional NAME)`

Rename a droplet with ID and NAME.

#### `(docean-snapshot-droplet ID &optional NAME)`

Snapshot a droplet with ID and NAME.

#### `(docean-droplet-list)`

Show user droplets.

#### `(docean-refetch-droplets)`

Refetch droplets information.

#### `(docean-action-list)`

Show user actions.

#### `(docean-refetch-actions)`

Refetch actions information.

-----
<div style="padding-top:15px;color: #d0d0d0;">
Markdown README file generated by
<a href="https://github.com/mgalgs/make-readme-markdown">make-readme-markdown.el</a>
</div>
