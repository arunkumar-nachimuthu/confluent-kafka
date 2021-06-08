# CONFLUENT-KAFKA
  A simple playbook to deploy a single node broker and zookeeper for development purposes.
  
## BEFORE YOU RUN
  * Export the below environmental variable to make sure ansible knows where your python interpreter is.
```shell
   export ANSIBLE_PYTHON_INTERPRETER=$(which python3)
```
  * Install requirements.txt using pip to make sure all the libraries are available.
```shell
   pip3 install -r requirements.txt
```
  * Make sure docker is up and running.

## HOW TO RUN
  * For deploying single node kakfa broker and zookeeper i,e all components of kafka, use the following command.
```shell
   ansible-playbook -i inventory.yml deploy-all.yml
```
  * For deploying either zookeeper or kafka, use one of the following command as needed.
```shell
   ansible-playbook -i inventory.yml zookeeper.yml
   ansible-playbook -i inventory.yml kafka.yml
```
   * Refer the following documents on how to provision topics.
## RESOURCES/REFERENCES
  * Confluent - https://docs.confluent.io/5.0.0/installation/docker/docs/installation/single-node-client.html
  * Confluent - https://github.com/confluentinc/cp-all-in-one/blob/6.1.1-post/cp-all-in-one/

