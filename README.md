# Airgap CF Templates

### airgap.json

* Spins up _**empty nodes**_ for testing airgapped installs of Chef products
* All nodes are accessible from internet
* None of the nodes can reach back out for packages, github repos, Gems etc

### Usage

* Log into AWS and open your "Cloud Formation" console
* Select create
* Select _**upload template**_ and select the ```airgap.json``` from this repo
* Set the stack name (it will be used in resource names)
* Select the SSH keypair you will use to log on to the machines
* (Optional) override the default AMI to select your base OS
* Spin it up baby yeah!!!

### What it spins up

* VPC
* Server subnet
* Internet gateway
* Route table
* Chef Server
* Delivery Server
* Supermarket Server
* Atrifactory Server
* Build nodes x3
* Application nodes x4
* A network ACL which is fairly open
* Restrictive (outbound) security groups for each machine type
