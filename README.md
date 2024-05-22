<h2><img align="middle" src="https://raw.githubusercontent.com/odb/official-bash-logo/master/assets/Logos/Icons/PNG/64x64.png" >
OctoPower - Easy JCB Powers to Composer PHP package
</h2>

With this script we can easily package multiple power classes in an automated way from a json configuration file, and environment variables into a composer package.

> program only for ubuntu/debian and Gitea systems at this time (should you like to use it on other OS's please open and issue...)
---
# Install
```shell
$ sudo curl -L "https://git.vdm.dev/api/v1/repos/octoleo/octopower/raw/src/octopower" -o /usr/local/bin/octopower
$ sudo chmod +x /usr/local/bin/octopower
```
---
# Usage
> To see the help menu
```shell
$ octopower -h
```
---
## Help Menu (octopower)
```txt
Usage: octopower [OPTION...]
	Options
	======================================================
   -p | --packager=<packager Name>
    Packager name
    example: octopower -p="Vast Development Method"
    ======================================================
   -pu | --packager-url=<//packager.url>
    Packager url
    example: octopower -pu="https://git.vdm.dev/"
    ======================================================
   -md | --main-dir=<path>
    load the main working directory
    example: octopower --main-dir=/src
    ======================================================
   -e | --env=<file>
    load the environment variables file
    example: octopower --env=/src/.env
    ======================================================
   --conf | --config=<path/url>
    load the configuration for the package in json format
       file-example: src/example.json
    example: octopower --config=config.json
    ======================================================
   -ld | --licence-dir=<path>
    load the licence directory
    example: octopower --licence-dir=/src/licence
    ======================================================
   -t | --token=<access_token>
    load the global token
    example: octopower --token=xxxxxxxxxxxxxxxxxxxxxxxxx
    ======================================================
   -u | --url=<gitea>
    Global url of the Gitea instance
    example: octopower --url="git.vdm.dev"
    ======================================================
   -a | --api=<//gitea.api>
    Global api of the Gitea instance
    example: octopower --api="https://git.vdm.dev/api/v1"
    ======================================================
   -q | --quiet
    mute all output messages
    example: octopower --quiet
    ======================================================
   --update
    to update your install
    example: octopower --update
    ======================================================
   --uninstall
    to uninstall this script
    example: octopower --uninstall
    ======================================================
   -h|--help
    display this help menu
    example: octopower -h
    example: octopower --help
    ======================================================
                    OctoPower v1.0.0
    ======================================================
```

### Local Environment Variables File

Give the path to your .env file to the program like this:
```shell
$ octopower --env="/home/username/.config/octopower/custom.env"
```
Or with an environment variable you set before using the program like this:
```shell
$ export VDM_ENV_FILE_PATH="/home/username/.config/octopower/custom.env"
```

> Default path is: /home/$USER/.config/octopower/.env

### API ACCESS TOKEN (never share your token)

You can set your API access token for Gitea via the .env file like this:
```shell
VDM_GLOBAL_TOKEN="xxxxxxxxxxxxxxxxxxxxxxxxx"
```
Or you can pass the token directly to the script like this:
```shell
$ octopower --token="xxxxxxxxxxxxxxxxxxxxxxxxx"
```
Or with an environment variable you set before using the program like this:
```shell
$ export VDM_GLOBAL_TOKEN="xxxxxxxxxxxxxxxxxxxxxxxxx"
```

### Configuration File

To see the example of the json configuration options check out [config/octopower.json](https://git.vdm.dev/octoleo/octopower/src/branch/master/config/octopower.json).

You can set your configuration file path via the .env file like this:
```shell
VDM_PACKAGE_CONF_FILE="/home/username/.config/octopower/package_name_config.json"
```
Or you can pass it to the program by URL:
```shell
$ octopower --conf="https://git.vdm.dev/api/v1/repos/octoleo/octopower/raw/config/octopower.json"
```
Or via a local file path:
```shell
$ octopower --conf="/home/username/.config/octopower/package_name_config.json"
```
Or with an environment variable you set before using the program like this:
```shell
$ export VDM_PACKAGE_CONF_FILE="/home/username/.config/octopower/package_name_config.json"
```

---
## Uninstall
```shell
$ octopower --uninstall
```
---
# Free Software License
```txt
@copyright  Copyright (C) 2021 Llewellyn van der Merwe. All rights reserved.
@license    GNU General Public License version 2; see LICENSE
```
