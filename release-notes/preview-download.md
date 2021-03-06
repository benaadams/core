# .NET Core 1.1 Preview 1

Download the installer or binary archive for your platform.

| .NET Core 1.1 Preview 1 | Installer                                        | Binaries                                        |
| ----------------------- | :----------------------------------------------: | :----------------------------------------------:|
| Windows                 | [32-bit](https://go.microsoft.com/fwlink/?LinkID=831458) / [64-bit](https://go.microsoft.com/fwlink/?LinkID=831453)  | [32-bit](https://go.microsoft.com/fwlink/?LinkID=831474) / [64-bit](https://go.microsoft.com/fwlink/?LinkID=831469) |
| macOS                   | [64-bit](https://go.microsoft.com/fwlink/?LinkID=831445)                           | [64-bit](https://go.microsoft.com/fwlink/?LinkID=831486)                          |
| CentOS 7.1              | -                                                         | [64-bit](https://go.microsoft.com/fwlink/?LinkID=831470)                          |
| Debian 8                | -                                                         | [64-bit](https://go.microsoft.com/fwlink/?LinkID=831481)                          |
| Fedora 23 / 24          | -                                                         | [64-bit](https://go.microsoft.com/fwlink/?LinkID=831489)                          |
| openSUSE 13.2           | -                                                         | [64-bit](https://go.microsoft.com/fwlink/?LinkID=831491)                          |
| openSUSE 42.1           | -                                                         | [64-bit](https://go.microsoft.com/fwlink/?LinkID=831475)                          |
| Ubuntu 14.04            | See notes below for Ubuntu 14.04 and Mint 17 installers   | [64-bit](https://go.microsoft.com/fwlink/?LinkID=831488)                          |
| Ubuntu 16.04            | See notes below for Ubuntu 16.04 and Mint 18 installers   | [64-bit](https://go.microsoft.com/fwlink/?LinkID=831471)                          |
| Ubuntu 16.10            | See notes below for Ubuntu 16.10                          | [64-bit](https://go.microsoft.com/fwlink/?LinkID=831479)                          |

## Installation from a binary archive

When using binary archives to install, we recommend the contents be extracted to /opt/dotnet and a symbolic link created for dotnet. If an earlier release of .NET Core is already installed, the directory and symbolic link may already exist.

```bash
sudo mkdir -p /opt/dotnet
sudo tar zxf [tar.gz filename] -C /opt/dotnet
sudo ln -s /opt/dotnet/dotnet /usr/local/bin
```

## Ubuntu installation

### Set up package source

The first step is to establish the source feed for the package manager. This is only needed if you have not previously set up the source or if you are installing on Ubuntu 16.10 for the first time.

***Note: Ubuntu feeds are not live yet. Will remove this note as soon as they are up and running.***

#### Ubuntu 14.04 and Linux Mint 17

```bash
sudo sh -c 'echo "deb [arch=amd64] https://apt-mo.trafficmanager.net/repos/dotnet-release/ trusty main" > /etc/apt/sources.list.d/dotnetdev.list'
sudo apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 417A0893
sudo apt-get install dotnet-sdk-1.0.0-preview2.1-003155
```

#### Ubuntu 16.04 and Linux Mint 18

```bash
sudo sh -c 'echo "deb [arch=amd64] https://apt-mo.trafficmanager.net/repos/dotnet-release/ xenial main" > /etc/apt/sources.list.d/dotnetdev.list'
sudo apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 417A0893
sudo apt-get install dotnet-sdk-ubuntu.16.04-x64.1.0.0-preview2.1-003155
```

#### Ubunt 16.10

```bash
sudo sh -c 'echo "deb [arch=amd64] https://apt-mo.trafficmanager.net/repos/dotnet-release/ yakkety main" > /etc/apt/sources.list.d/dotnetdev.list'
sudo apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 417A0893
sudo apt-get install dotnet-sdk-ubuntu.16.10-x64.1.0.0-preview2.1-003155
```

Now that the source feed is defined for your distro, apt-get update can be used to install the latest available version.

```bash
sudo apt-get install
```






