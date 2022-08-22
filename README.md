# Install and configure Turbonomic Virtual Machine at IBM Cloud VPC

Pre req: Setup Turbonomic virtual machine ( [Turbonomic Terraform](https://github.com/jpmenegatti/ibmcloud_terraform_turbonomic) )

IBM Cloud Schematics Actions Ansible script to install and configure Turbonomic

## Creating the playbook in Schematics by using console

1. Open the [Schematics action configuration page](https://cloud.ibm.com/schematics/actions/create?name=deployapp&url=https://github.com/Cloud-Schematics/ansible-app-deploy-iks).
2. Review the name for your action, and Repository URL are pre-populated, optionally, you can enter an the unique name for an **Action name** (suggestion ibmcloud_act_turbonomic).
3. Review the resource group and location where you want to create an action. 
4. Click the **Create** button, and allow to retrieve your playbook details.
5. Click **Retrieve playbook** button to view the playbook list.
6. Select the `setup.yml` playbook.
7. Select the **Verbosity** level to control the depth of log information to display. For example, enter `4` to check detailed log information. Refer to [create an action](https://cloud.ibm.com/docs/schematics?topic=schematics-action-setup#create-action) for more information.
8. Click **Save**.

## Inventory

1. Create a new Ansible inventory. (Suggestion: define manually using Turbonomic public IP)
2. Use private SSH key supplied with Turbonomic image in the inventory configuration
3. Click **Save**.

## Running the playbook in Schematics by using console
1. Click **Run action**.
