<h1>Create Virtual Machine Template</h1>

This job will create a virtual machine in an existing AWS VPC as described in the collection [readme](https://github.com/ansible-content-lab/aws.infrastructure_config_demos/blob/main/README.md).

1. Click the **Templates** link under **Resources** in the left menu.
2. Click the **Add** button, then **Add job Template**.
3. Fill the following fields:
    1. **Name**: ```AWS - Create RHEL 8 VM```
    2. **Job Type**: Run
    3. **Inventory**: Demo Inventory
    4. **Project**: AWS - Content Lab Infrastructure Config Demos
    5. **Playbook**: playbook_create_vm.yml
    6. **Credentials**: AWS - Access Key
    7. **Variables, please check Prompt on launch**.  **This is because some of these values wont be available until later AFTER you run the AWS - Create Transit Network job template.**

```
---
vm_blueprint: rhel8
create_vm_aws_keypair_name: <your-initials>-aaponaws-<monthyear> # Replace with the name of the AWS SSH key that you created at the start of this exercise
create_vm_aws_securitygroup_name: dmz-sg
create_vm_aws_vpc_subnet_name: dmz-subnet
create_vm_aws_region: <your-aws-region>
```

The finished Variable section will look like the following:

```
---
vm_blueprint: rhel8
create_vm_aws_keypair_name: jag-aaponaws-aug23
create_vm_aws_securitygroup_name: dmz-sg
create_vm_aws_vpc_subnet_name: dmz-subnet
create_vm_aws_region: us-east-2
```




4. Click **Save** at the bottom of the screen.

# [NEXT - Delete Virtual Machine](page11.md)
