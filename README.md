#Let's begin exploring "KOPS"


#I am going to begin with v1.23.2 of KOPS.

# Points to be noted - 
Support for Kubernetes version 1.17 has been removed.

Support for the Lyft CNI has been removed.

The Weave CNI is not supported for Kubernetes 1.23 or later.

Support for CentOS 7 has been removed.

Support for CentOS 8 has been removed (replaced by Rocky Linux 8).

Support for Debian 9 has been removed.

Support for RHEL 7 is has been removed.

Support for Ubuntu 16.04 (Xenial) has been removed.

Cilium now has disable-cnp-status-updates: true by default. Set this to false if you rely on the CiliumNetworkPolicy status fields.


# Create IAM role for instance with permissions -
  -AmazonEC2FullAccess
  <br />
  -AmazonRoute53FullAccess
  <br />
  -AmazonS3FullAccess
  <br />
  -IAMFullAccess
  <br />
  -AmazonVPCFullAccess
  <br />
  -AmazonSQSFullAccess
  <br />
  -AmazonEventBridgeFullAccess


# Create ec2 Instance for Kops-workstation 
## You can choose any instance type as long it's supported
  Icon name: computer-vm 
  <br />
           Chassis: vm 
           <br />
        Machine ID: 2d99ef724dce45369047869bf2504a0b 
        <br />
           Boot ID: 9666ed65a0de48c89b72e81e54ba4a8e
           <br /> 
    Virtualization: xen
    <br /> 
  Operating System: Amazon Linux 2 
  <br />
       CPE OS Name: cpe:2.3:o:amazon:amazon_linux:2
       <br /> 
            Kernel: Linux 5.10.109-104.500.amzn2.x86_64
            <br /> 
      Architecture: x86-64 


# Install Binary
file -  kops-linux-amd64

```
wget https://github.com/kubernetes/kops/releases/download/v1.23.2/kops-linux-amd64
  
```




