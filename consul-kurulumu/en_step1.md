# HashiCorp - Consul
In scenario 2 of our Consul tutorial, we will learn how the Consul software is installed on our machine and how the service agent is started.
### 1-Consul Server Installation
Before starting the installation of our Consul software, we need to update the Ubuntu package manager. For this, run the following commands in order:

`apt-get update -y`

Install the packages we need in the Consul installation using the following command:

`apt-get install unzip gnupg2 curl wget -y`

Before we move on to the next step, let's examine the components of the above command:
- **apt-get:** Uses the APT tool, which is the package manager for Ubuntu-based Linux distributions.
- **unzip:** Used to extract ZIP files.
- **gnupg2:** is an open source encryption software called GNU Privcy Guard.
- **curl:** A tool for exchanging data using URLs from the command line.
- **wget:** Used to download files over the Internet.
- **-y:** It is an option to automatically install packages without any confirmation during the process.

After the necessary packages are installed, let's get the latest version of the Consul software:

`wget https://releases.hashicorp.com/consul/1.8.4/consul_1.8.4_linux_amd64.zip`

After the installation is complete, let's open the file:

`unzip consul_1.8.4_linux_amd64.zip`

Next, let's move the consul file to */usr/local/bin/*:

`mv consul /usr/local/bin/`

After completing the file migration, we are now ready to use the consul software. (If you want to make sure the consul software is installed, you can use the `consul --version`command.)

-> You can proceed to the next step where we will learn what the Service Agent used with Consul is and why it is used.