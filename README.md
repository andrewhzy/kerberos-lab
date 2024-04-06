# kerberos-lab
try kerberos, try client accessing from another VPC 

1. set up kerberos environment in aws
   1. an instance for kerberos: krbtest-krb
   2. an instance for zookeeper: krbtest-zk
   3. an instance for zookeeper client: krbtest-clt
2. install apps on instances respectively.
3. protect zk server with kerberos
4. try connecting to zk server from krbtest-clt instance.