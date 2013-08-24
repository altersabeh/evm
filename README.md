# EVM - Erlang Version Manager

This is a simple script which aims to make easy the management of different Erlang versions in your system.

## Installation

Simply execute:

    $ ./install

And then add the following line to your .bashrc file:

    source $HOME/.evm/scripts/evm

This will create some directories inside your $HOME/.evm dir:

- **erlang_tars** : the place where all erlang tarballs downloaded by evm will be cached.
- **erlang_versions** : where the erlang enviroment will be installed.
- **scripts** : the location of evm script itself.
- **evm_config** : contains a single file pointing the current _default_ erlang version in use.

## Usage

**EVM** is based on **RVM** (<https://rvm.io>), but of course without that so many features.
It will help you to have as many erlang versions you like in your system, switching between them as easy as possible.

After the installation, you can check if everything is ok by executing:

    $ evm help

If that executes fine, then you'll should have a list of actions you can execute:

- *list* (`$ evm list`)
    This will fetch all the available erlang tarball versions from <http://www.erlang.org/download.html> presenting you a list of them.

- *install* (`$ evm install <version>`)
    This will download the erlang tarball identified by *version* ( if not yet downloaded ) and then it will simply execute **./configure - make - make install** passing some default values.

    It will also give you a chance to download any erlang dependency you need, by stopping the process after the **./configure** command has finished.

    **Obs:**: EVM *will not* downalod the erlang dependencies for you.

- *installed* (`$ evm installed`)
- *download* (`$ evm download`)
- *remove* (`$ evm remove`)
- *uninstall* (`$ evm uninstall`)
- *cache* (`$ evm cache`)
- *system* (`$ evm system`)
- *use* (`$ evm use`)
- *help* (`$ evm help`)

## EVM help

    EVM Home: 
        /home/robison/.evm
    Default Version:
        R15B01
    Versions Ready To Use: 
        R16B
        R15B01

    Usage:
        * evm list
            Lists available erlang versions which can be downloaded and installed on the system.
        * evm cache
            Lists available erlang versions which are in the evm space and not necessarily installed.
        * evm download [version]
            Downloads the erlang version.
        * evm install [version]
            Downloads and installs the specified erlang version.
        * evm installed
            Lists erlang versions which are built and are ready to be used.
        * evm use [version]
            Begins to use the specified erlang version.
        * evm default [version]
            Makes the specified erlang version as the default erlang version.
        * evm remove [version]
            Removes the erlang version completely from the evm space.
        * evm uninstall [version]
            Uninstalls erlang but keeps the erlang version within the evm.
        * evm system
            Alters the PATH within the shell to use the non-evm erlang


## Dependencies

This script is dependent on :

- *lynx* (<http://lynx.isc.org/>)
- *wget*

## Contributing

1. Fork it
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Added some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create new Pull Request
