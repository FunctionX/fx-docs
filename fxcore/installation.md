# Installation f(x)Core

This guide will explain how to install the `fxcored` CLI onto your system. With this installed on a server, you can participate on the mainnet as either a [Full Node](setup-node/) or a [Validator](../validators/validator-setup.md).

Additionally, you may refer to this [<mark style="color:red;">**YouTube tutorial video**</mark>](https://www.youtube.com/watch?v=Fz0Y3qKG9og\&ab\_channel=FunctionX) to set up your validator.

## Hardware Requirements

We recommend the following for running f(x)Core:

* 4 or more CPU cores
* At least 500G of disk storage
* At least 8G of memory
* At least 10mbps network bandwidth

To see a [quick cloud setup](../fxcore-tutorials/cloud-setup.md) on how to setup and deploy it on the cloud.

## Install build requirements

Install `make` and `gcc`.

On Ubuntu this can be done with the following commands:

{% tabs %}
{% tab title="Ubuntu" %}
```
sudo apt-get update
```

```
sudo apt-get install -y make gcc
```

> Ps: `sudo apt-get install -y make gcc` may have encountered a problem with locked files, just try `sudo apt-get install -y make gcc` again.
{% endtab %}

{% tab title="Mac" %}
Ensure you have [Homebrew](https://brew.sh/) installed.

Once you have Homebrew installed, you may run the following commands to install `make` :

```
brew install make
```

and `gcc`:

```
brew install gcc
```

We'll be needing these commands later so let's install the necessary packages:

```
brew install git
```

```
brew install wget
```
{% endtab %}

{% tab title="Windows" %}
You will need to run git bash. You may find the installation link [here](https://git-scm.com/download/win).

Ensure you have `make` and `gcc` installed and that the paths are set correctly for git bash.

One option for installing `gcc` can be found [here](https://jmeubank.github.io/tdm-gcc/articles/2021-05/10.3.0-release).

{% hint style="info" %}
You may select tdm64-gcc-10.3.0-2

Restart gitbash after installing
{% endhint %}

One option for installing `make` is using `chocolate` , more information can be found [here](https://chocolatey.org/install).

Once you have chocolate installed, run this command:

{% hint style="info" %}
make sure to run gitbash as administrator mode if the following commands do not work
{% endhint %}

```
choco install make
```

Ensure you have all the necessary dependencies and compilers.

```
gcc --version
```

will return:

```
gcc.exe (tdm64-1) 10.3.0
Copyright (C) 2020 Free Software Foundation, Inc.
This is free software; see the source for copying conditions.  There is NO
warranty; not even for MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE
```

and for make:

```
make --version
```

will return:

```
GNU Make 4.3
Built for Windows32
Copyright (C) 1988-2020 Free Software Foundation, Inc.
License GPLv3+: GNU GPL version 3 or later <http://gnu.org/licenses/gpl.html>
This is free software: you are free to change and redistribute it.
There is NO WARRANTY, to the extent permitted by law.
```
{% endtab %}
{% endtabs %}

## Install Go

{% tabs %}
{% tab title="All other environments" %}
Install `go` by following the [official docs](https://golang.org/doc/install). Please select your respective environment❗

> For Ubuntu environment, there may be `permissions denied` issues with unzipping the go zip file, try using `sudo su` to resolve it.
{% endtab %}

{% tab title="If you are remoting into a terminal" %}
Especially if you are remoting into a Ubuntu terminal, run this command to download the `go` installer:

```
wget -c https://dl.google.com/go/go1.20.3.linux-amd64.tar.gz
```

{% hint style="info" %}
After you have downloaded the package and you may proceed to step 2 of the [official docs](https://golang.org/doc/install). Choose your system OS and follow the instructions stated.
{% endhint %}
{% endtab %}
{% endtabs %}

{% hint style="info" %}
**Go 1.19+** or later is required for the f(x)Core. If you are remoting into a terminal, you may input the following command:
{% endhint %}

Setting environment variables:

```
mkdir -p $HOME/go/bin
echo "export PATH=$PATH:/usr/local/go/bin" >> ~/.profile
echo "export PATH=$PATH:$(go env GOPATH)/bin" >> ~/.profile
source ~/.profile
```

## Install the binaries

Next, let's install the latest version of f(x)Core. Make sure you have git installed if not you will be prompted to `install git`. Follow the instruction in the terminal.

{% tabs %}
{% tab title="Mainnet" %}
```
git clone --branch release/v3.1.x https://github.com/functionx/fx-core.git
```

```
cd fx-core
```
{% endtab %}

{% tab title="Testnet" %}
```
git clone --branch release/v3.1.x https://github.com/functionx/fx-core.git
```

```
cd fx-core
```
{% endtab %}

{% tab title="Windows" %}
{% hint style="info" %}
You should run your commands in gitbash. But open fxcored.exe file using cmd prompt

Make sure the name of your folder does not have whitespaces!
{% endhint %}

```
git clone --branch release/v3.1.x https://github.com/functionx/fx-core.git
```

```
cd fx-core
```

```
```
{% endtab %}
{% endtabs %}

{% hint style="info" %}
You may find the latest branches here: [https://github.com/FunctionX/fx-core/branches](https://github.com/FunctionX/fx-core/branches)
{% endhint %}

{% tabs %}
{% tab title="All Other Environments " %}
```
make go.sum
```

```
make install
```
{% endtab %}

{% tab title="Windows " %}
```
make go.sum
```

```
make build-win
```

{% hint style="info" %}
use cmd prompt to open the fxcored.exe file

in the path ./build/bin/fxcored.exe
{% endhint %}
{% endtab %}
{% endtabs %}

That will install the `fxcored` binary. Verify version:

{% tabs %}
{% tab title="Long version" %}
```
fxcored version --long
```
{% endtab %}

{% tab title="Short version" %}
```
fxcored version
```
{% endtab %}
{% endtabs %}

`fxcored version --long` should output something similar to:

```
name: fxcore
server_name: fxcored
version: release/vx.x.x xxx
commit: xxx
build_tags: netgo,ledger
go: go version go1.19 darwin/amd64
build_deps:
...
cosmos_sdk_version: v0.xx.x
```

### Build Tags

Build tags indicate special features that have been enabled in the binary.

| Build Tag | Description                                     |
| --------- | ----------------------------------------------- |
| netgo     | Name resolution will use pure Go code           |
| ledger    | Ledger devices are supported (hardware wallets) |
