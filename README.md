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
AmazonEC2FullAccess
AmazonRoute53FullAccess
AmazonS3FullAccess
IAMFullAccess
AmazonVPCFullAccess
AmazonSQSFullAccess
AmazonEventBridgeFullAccess


