# kerberos-lab
try kerberos, try client accessing from another VPC.

1. set up kerberos environment in aws.
   1. an instance for kerberos: krbtest-krb.
   2. an instance for zookeeper: krbtest-zk.
   3. an instance for zookeeper client: krbtest-clt.
2. install apps on instances respectively.
   1. install kerberos on krbtest-krb
      1. sudo yum update -y
      2. sudo yum install -y krb5-server krb5-libs krb5-workstation
      3. config krb5.conf
      4. Initialize the KDC database with a master key: 
         1. sudo kdb5_util create -s
         2. Enter KDC database master key: zookeeper
3. protect zk server with kerberos.
4. connecting to zk server from krbtest-clt instance.
5. connecting to zk from another VPC.