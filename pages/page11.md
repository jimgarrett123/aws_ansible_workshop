<h1>Delete Virtual Machine (EC2 Instance)</h1>

1. Click the **Templates** link under **Resources** in the left menu.
2. Click the **Add** button, then **Add job Template**.
3. Fill the following fields:
    1. **Name**: ```AWS - Delete RHEL 8 VM```
    2. **Job Type**: Run
    3. **Inventory**: Demo Inventory
    4. **Project**: AWS - Content Lab Infrastructure Config Demos
    5. **Playbook**: playbook_delete_vm.yml
    6. **Credentials**: AWS - Access Key
    7. **Variables (prompt on launch checked)**:

```
---
aws_region: <your-aws-region> # Replace with your region
```


4. Click **Save** at the bottom of the screen.

# [NEXT - Ansible Automation Controller Functionality](page12.md)
