## Let's begin exploring "KOPS in AWS"


## I am going to begin with v1.23.2 of KOPS.

# Prerequisite to install
 - AWS CLI (url -https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html )
 - Kubectl (url - https://kubernetes.io/docs/tasks/tools/install-kubectl-linux/)

# Breaking news from KOPS - 
Support for Kubernetes version 1.17 has been removed.

Support for the Lyft CNI has been removed.

The Weave CNI is not supported for Kubernetes 1.23 or later.

Support for CentOS 7 has been removed.

Support for CentOS 8 has been removed (replaced by Rocky Linux 8).

Support for Debian 9 has been removed.

Support for RHEL 7 is has been removed.

Support for Ubuntu 16.04 (Xenial) has been removed.

Cilium now has disable-cnp-status-updates: true by default. Set this to false if you rely on the CiliumNetworkPolicy status fields.


# Create IAM role for instance with permissions shown below and attach once instance is created -
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
    Virtualization: xen
    <br /> 
  Operating System: Red Hat Enterprise Linux 8.6 (Ootpa) 
  <br />
       CPE OS Name: cpe:/o:redhat:enterprise_linux:8::baseos
       <br /> 
            Kernel: Linux 4.18.0-372.9.1.el8.x86_64
            <br /> 
      Architecture: x86-64 


# Install Kops
file -  kops-linux-amd64

```
wget https://github.com/kubernetes/kops/releases/download/v1.23.2/kops-linux-amd64

sudo mv kops-linux-amd64  /usr/local/bin/kops

sudo chmod +x /usr/local/bin/kops
```  

# Create s3 bucket 

```
aws s3 mb s3://<unique-bucket-name>
```

# environment variables

Check the type of your shell before editing, in this case it's bash. 

```
vi .bashrc

```
Add unique name and s3 bucket in the file - 

```
export NAME=rashedk.k8s.local  #kubernetes cluster name
export KOPS_STATE_STORE=s3://rashedk.k8s.local






