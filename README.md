# ETB Ethereum ToDo List

## Activating on Azure

After activating your Azure account, search for DevTest Labs. Enter a name and location (closest to you) and deploy.

Next, click '+Virtual Machine' to add your Ethereum virtual machine and configuration:

- Select “Ubuntu Server 14.04 LTS” as the base image 
- Give the machine a name, i.e. EthNode1 
- Provide a username and password 
- Set a machine size eg Standard_D2_v2 
- VirtualNetwork and Subnet should be preconfigured. Leave the IP address as public 
- Click on “Artifacts” to add the required Ethereum components 

## Connect to the Virtual Machine

- Select “Go-Ethereum-Homestead” 
- In the blade that appears, enter the username you created earlier into the Admin User Account field 
- Click Add on the artefact configuration (username) blade 
- Click OK on the “Add artifacts” blade 
- Click Create on the “Virtual Machine” blade which will now have 1 artifact selected

Then connect to the virtual machine via SSH:

- In the DevTest Lab blade, click through to the VM you want to connect to
- - Note the auto-start and auto-shutdown tile. You can opt-in to have your VMs automatically shutdown out of hours ensuring they don’t incur unnecessary costs 
- Capture the public IP address of the VM so we can connect to it over SSH.

## Deploy the DApp

Open a connection and log in with the credentials you used, i.e. sharonl@ethnode2438421.eastus.cloudapp.azure.com

Git clone this repository and navigate to the directory.

Download https://nodejs.org/en/

Install Truffle

``
npm install –g truffle
``

Install Ethereum Testrpc

``
npm install –g ethereumjs-testrpc
``

If you don't have Node v8.9.0 or NPM v4.0.5​

Download https://nodejs.org/en/​

Open terminal and start 

``
$ testrpc
``

Open another terminal and run

``
$ npm install
``

Start the app with 

``
$ npm start
``

Navigate to 'localhost:3000' to see your app!

## Credits
* Eat The Blocks [website](https://eattheblocks.com)
* Eat The Blocks [YouTube Channel](https://www.youtube.com/channel/UCZM8XQjNOyG2ElPpEUtNasA)
* Truffle framework [website](http://truffleframework.com)
* Ethereumjs testnet [website](https://www.npmjs.com/package/ethereumjs-testrpc)
* Solidity docs [website](https://solidity.readthedocs.io/en/develop)
