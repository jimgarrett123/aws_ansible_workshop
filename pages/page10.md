<h1>Create Virtual Machine Template</h1>

This job will create a virtual machine in an existing AWS VPC as described in the collection [readme](https://github.com/ansible-content-lab/aws.infrastructure_config_demos/blob/main/README.md).

1. Click the �**Templates**� link under �**Resources**� in the left menu.
2. Click the �**Add**� button, then �**Add job Template**�.
3. Fill the following fields:
    1. **Name**: AWS - Create RHEL 8 VM
    2. **Job Type**: Run
    3. **Inventory**: Demo Inventory
    4. **Project**: AWS - Content Lab Infrastructure Config Demos
    5. **Playbook**: playbook_create_vm.yml
    6. **Credentials**: AWS - Access Key
    7. **Variables, please check �Prompt on launch�**.  **This is because some of these values won�t be available until later AFTER you run the �AWS - Create Transit Network� job template.**

```
---
aws_region: <your-aws-region>
aws_keypair_name: <your-initials>-aaponaws-<monthyear>
aws_instance_size: <instance-size>
vm_blueprint: rhel8
vm_name: demo_vm
vm_deployment: ansible
vm_purpose: create-vm-demo
ansible-role: create_vm
ansible-collection: aws.infrastructure_config_demos
```

The finished Variable section will look like the following:

```
---
aws_region: us-east-2
aws_keypair_name: jag-aaponaws-march2023
aws_instance_size: t2.micro
vm_blueprint: rhel8
vm_name: demo_vm
vm_deployment: ansible
vm_purpose: create-vm-demo
ansible-role: create_vm
ansible-collection: aws.infrastructure_config_demos
```



<table>
  <tr>
   <td><strong>AWS Region</strong>
   </td>
   <td><strong>RHEL AMI</strong>
   </td>
  </tr>
  <tr>
   <td>eu-central-1
   </td>
   <td>ami-0e7e134863fac4946
   </td>
  </tr>
  <tr>
   <td>us-east-1
   </td>
   <td>ami-06640050dc3f556bb
   </td>
  </tr>
  <tr>
   <td>us-east-2
   </td>
   <td>ami-092b43193629811af
   </td>
  </tr>
  <tr>
   <td>us-west-1
   </td>
   <td>ami-0186e3fec9b0283ee
   </td>
  </tr>
  <tr>
   <td>us-west-2
   </td>
   <td>ami-08970fb2e5767e3b8
   </td>
  </tr>
</table>




4. Click �**Save**� at the bottom of the screen.

[NEXT - Delete Virtual Machine](page11.md)