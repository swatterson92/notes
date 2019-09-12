## What is terraform? 

 - Infrastructure as code 

 - Enables the automation of your infrastructure( hardware)

 - Terraform will keep your infrastructure in a certain state (e.g 2 web instances, with 2 volumes and 1 load balancer)

 - Makes your infrastructure able to be audited.

## What is Terraform used for? 

 - Used to automate the provisioning of the infrastructure itself. (via AWS/AZURE/Digital )

 - Should NOT be used to automate the installation and configuration of software. This is what Ansible, Chef and Puppet are used for. 

 - Terraform and Ansible generally play well together. Terraform provisions the HW, Ansible installs and configures the software. 

 ## Terraform Basics - Commands

### terraform init

 - Initializes and installs any modules required for a tf file to be ran. 

 - Prompts the user to upgrade terraform if applicable. 

### terraform plan

 - Allows tf files to be validated. 

 - Gives the user a preview of what is going to be provisioned, but does not actually provision it.

### terraform destroy

 - Will tear down instances that have been spun up based on the content of the tf files. 

### terraform apply 

- Will execute the contents of the terraform file and provision the infrastructure noted in terraform. 

- Will output a state file which is the state of affairs after the terraform script has executed. 

- That state file is required when modifying or destroying the infrastructure. 


## Terraform Basics - Variables

 - Used to store things that may change. AMI's for example change over time, so important to be able a single point of contact to replace these if needed.

 - Also should be used for Storing Secrets and other sensitive data. 

 - If you don't feel safe committing it it, you should put it in a variable.

 -  Declared in a var.tf file like this : 

                variable MY_PASSWORD {}

-  Values are set in a tfvars file like this: 

    MY_PASSWORD = "My super secret password is here"


