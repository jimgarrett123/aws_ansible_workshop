<h1>Create Job Templates</h1>

<h2>Create Transit Peer Network</h2>

This job will deploy a transit peering network model as described in the collection [readme](https://github.com/ansible-content-lab/aws.infrastructure_config_demos/blob/main/roles/manage_transit_peered_networks/README.md).

1. Click the “**Templates**” link under “**Resources**” in the left menu.
2. Click the “**Add**” button, then “**Add job Template**”.
3. Fill the following fields:
    1. **Name**:
```AWS - Create Transit Network```
    2. **Job Type**: Run
    3. **Inventory**: Demo Inventory
    4. **Project**: AWS - Content Lab Infrastructure Config Demos
    5. **Playbook**: playbook_create_transit_network.yml
    6. **Credentials**: AWS - Access Key
    7. **Variables**: Add the below to the Variables window frame.

```
---
aws_region: <your-aws-region> # replace with your region
priv_network_instance_ami: ami-06640050dc3f556bb # Replace with the proper RHEL AMI for your region. A table of AMIs is below.
dmz_instance_ami: ami-06640050dc3f556bb # Replace with the proper RHEL AMI for your region. A table of AMIs is below.
dmz_ssh_key_name: <your-initials>-aaponaws-<monthyear> # replace with the name of the AWS SSH key that you created at the start of this exercise
priv_network_ssh_key_name: <your-initials>-aaponaws-<monthyear> # replace with the name of the AWS SSH key that you created at the start of this exercise
```

When finished, the variable section will look like the following:

```
---
aws_region: <your-aws-region>
priv_network_instance_ami: ami-<your-region-ami#>
dmz_instance_ami: ami-<your-region-ami#>
dmz_ssh_key_name: <your-initials>-aaponaws-<monthyear>
priv_network_ssh_key_name: <your-initials>-aaponaws-<monthyear>
```

My example is:

```
---
aws_region: us-east-1
priv_network_instance_ami: ami-06640050dc3f556bb
dmz_instance_ami: ami-06640050dc3f556bb
dmz_ssh_key_name: hm-aaponaws-jan2023
priv_network_ssh_key_name: hm-aaponaws-jan2023
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

4. Click “**Save**” at the bottom of the screen.
***
<h1>Delete Transit Network</h1>

1. Click the “**Templates**” link under “**Resources**” in the left menu.
2. Click the “**Add**” button, then “**Add job Template**”.
3. Fill the following fields:
    1. **Name**:  ```AWS - Delete Transit Network```
    2. **Job Type**: Run
    3. **Inventory**: Demo Inventory
    4. **Project**: AWS - Content Lab Infrastructure Config Demos
    5. **Playbook**: playbook_delete_transit_network.yml
    6. **Credentials**: AWS - Access Key
    7. **Variables**:

```
---
aws_region: <your-aws-region> # Replace with your region
```


4. Click “**Save**” at the bottom of the screen.

[NEXT - Create Virtual Machine Template](page10.md)

