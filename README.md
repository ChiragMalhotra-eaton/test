## `app` module
#### Represents a bare-bone application deployment. The `app` module output `config` (so-called umbilical cord) is used as input configuration for the addons.   

```terraform
module "app" {
  source = "sgi/app"

  platform = module.platform
}
```

### Prerequisites
 - The application repository must be declared in [repositories](https://dev.azure.com/SGICanDevOps/InfrastructureAsCode/_git/terraform-azuredevops?version=GBmain&path=%2Frepositories) using the [git_repository](https://dev.azure.com/SGICanDevOps/InfrastructureAsCode/_git/terraform-azuredevops?version=GBmain&path=%2Fmodules%2Fgit_repository) module in the corresponding project file. 
   The repository configuration creates a Kubernetes namespace where Kubernetes networking infrastructure and application components will be deployed. 

### Dependencies
 - [platform](https://dev.azure.com/SGICanDevOps/InfrastructureAsCode/_git/terraform-platform)

### Parameters
 - `platform` (required) - predefined platform configuration (the output of the `platform` module)
 
![Model View Controller](https://media.geeksforgeeks.org/wp-content/cdn-uploads/20210101201653/PDF.pdf)
