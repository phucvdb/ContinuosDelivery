# ContinuosDelivery
Build the steps for continous delivery on DevOps

I. For deploying on the VMs

I think the steps that should be excuted sequentially as below:

(1) Create the VMs --> (2) setup runtime environment --> (3) push the application binary file into VMs --> (4) push the application' data and configuration file into VMs --> (5) Start the App instances

To implements steps (1) and (5), you can use IaaS's apis (Openstack, AWS, ...), some Metadata as a Service layers's apis (Ubuntu MaaS, Foreman,...) or some orchestration tools ( Puppet, Ansible,...)
With the rest steps, maybe Orchestration tool are a good choice for creating a automatically workflow.
So in this guide, i will use the orchestration tools and IaaS'Api to excute the above workflow from (1) to (5)

I identify that some technical problems need to be solved before to create the workflow, as:

1. How to run scripts remotely into VMs after VMs creation based on pre-define scripts ( with YAML, XML format)

2. What way to get data and configuration files inside VMs ?
