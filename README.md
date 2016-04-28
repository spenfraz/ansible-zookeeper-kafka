# ansible-zookeeper-kafka
Zookeeper ensemble + Kafka cluster on CentOS EC2 via Ansible


Note: supports variable sized Zookeeper ensemble or Kafka cluster

Purpose: To automate configuration of (manually created) EC2 instances. 

    
    
             Via Amazon:
    * manually create EC2 instances (with default (CentOS) linux ami)
    * edit security groups to allow inbound communication (tcp) among Zookeeper instances
    * edit security groups to allow inbound communication (tcp) on Zookeeper instances from Kafka instances
    
    
        within hosts file add:
    * ip addresses of "kafka" instances 
    * ip addresses of "zookeeper" instances
    * path to .pem file
    
    

      
  
