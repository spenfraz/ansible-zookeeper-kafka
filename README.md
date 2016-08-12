# ansible-zookeeper-kafka
Zookeeper ensemble + Kafka cluster on CentOS EC2 via Ansible


Note: supports variable sized Zookeeper ensemble and Kafka cluster

Purpose: To automate configuration of (manually created) EC2 instances. 

    
### 1. Create an AWS account
   --> https://www.youtube.com/watch?v=WviHsoz8yHk
    
### 2. Manually create EC2 instances (with default (CentOS) linux ami)
   --> https://aws.amazon.com/getting-started/tutorials/launch-a-virtual-machine/
    
### 3-4. Edit security groups to allow inbound communication (tcp) among Zookeeper instances & Edit security groups to allow inbound communication (tcp) on Zookeeper instances from Kafka instances

   --> http://docs.aws.amazon.com/AWSEC2/latest/UserGuide/using-network-security.html#ec2-classic-security-groups
   
   --> https://www.youtube.com/watch?v=925n0IykcMA

### 5. Install Ansible
   --> http://docs.ansible.com/ansible/intro_installation.html#installation
   
   --> http://docs.ansible.com/ansible/intro_installation.html#control-machine-requirements

### 5. Clone this Repo 
         $ git clone https://github.com/spenfraz/ansible-zookeeper-kafka.git
         $ cd ansible-zookeeper-kafka
   
### 5. Edit hosts file
    within hosts file add:
    -ip addresses of "kafka" instances 
    -ip addresses of "zookeeper" instances
    -path to .pem file

    host file should read:
     
         [kafka_servers]
         <ip_of_kafka1-ec2> ansible_ssh_private_key_file=</path/to/key/file.pem> ansible_ssh_user=ec2-user
         <ip_of_kafka2-ec2>
         <ip_of_kafka3-ec2>
                 
         [zoo_servers]
         <ip_of_zoo1-ec2> ansible_ssh_private_key_file=</path/to/key/file.pem> ansible_ssh_user=ec2-user
         <ip_of_zoo2-ec2>
         <ip_of_zoo3-ec2>
                 
### 6. 
    

      
  
