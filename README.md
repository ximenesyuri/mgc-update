# About

`mgc-update` is a shell script defining a function that extends that provided by [mgc](https://github.com/MagaluCloud/mgccli) (the CLI of [Magalu Cloud](https://magalu.cloud/), a Brazilian public cloud) with the option `--update`, which install/update `mgc` to its latest version.

# Install

Just clone the repository and source the script `mgc-update` in your `.bashrc`:

```bash
git clone https://github.com/ximenesyuri/mgc-update /path/to/your/best/location
echo "source /path/to/your/best/location/mgc-update" >> $HOME/.bashrc
```

# Envs

```
env                 meaning                                     values                                     default
-------------------------------------------------------------------------------------------------------------------------     
MGC_AUTO_UPDATE     check for update before exec each cmd       true                                       empty
MGC_LOCATION        path to the dir to install/update mgc       any valid path included in your $PATH      /usr/bin
MGC_ARCHITECTURE    your UNIX architecture                      darwin_amd64                               linux_amd64
                                                                freebsd_amd64
                                                                linux_amd64
                                                                linux_arm64                    
```

# Usage

Use `mgc` normally, now with the additional option `--update`, which will verify and install the latest `mgc` version in the defined `MGC_LOCATION` for the defined `MGC_ARCHITECTURE`.

> **OBS.** If MGC_AUTO_UPDATE="true", then a verification for updates will be made before executing any `mgc` command.
