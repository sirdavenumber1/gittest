# Tutorial - Build Docker Image and run containers with embedded Control-M Agent
The content in this folder describes one specific implementation for building a Docker image with an embedded Control-M Agent. When instantiating containers, they connect to a Control-M environment and process work. The tutorial describes a method for specifying the target environment dynamically so that the same image can be connected to a test, dev, QA or production environment. The binding to the target environment is achieved by dynamically accessing endpoint information. 

File|Description
---------|-------
AgentCleanup.json|Control-M job to execute cleanup script
cleanup_ctmAgents_in_terminated_containers.sh|bash script to remove zombie agents from hostgroups and disconnect them from Control-M
Create_Docker_Image_with_Agent_Run_Container.txt|Commands used in the tutorial
decommission_controlm.sh|script inside a container used to remove agent form hostgroup and disconnect from Control-M prior to container termination
Dockerfile|used to build the image
MultiContainerSampleFlow.json|Job flow demonstrating jobs running across multiple containers in hostgroup
run_register_controlm.sh|script invoked when container starts to register with Control-M and add to desired hostgroup

See the [Automation API - Services](https://docs.bmc.com/docs/display/public/workloadautomation/Control-M+Automation+API+-+Services) documentation for more information.  
See the [Automation API - Code Reference](https://docs.bmc.com/docs/display/public/workloadautomation/Control-M+Automation+API+-+Code+Reference) documentation for more information.
