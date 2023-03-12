# helm-chart.templates
This is a sample template repository to create a helm chart without going lengths to install helm package on your machine.

Using the "use this template" option from this repository you will be able to create the necessary helm file contents and folders on the go and also creates a PR for owners to update/review code.

This is achieved using [GitHub Actions](https://docs.github.com/en/actions). GitHub Actions allow you to customize your workflows to meet the unique needs of your application and team.

## **Pre-requisites**
Some degree of knowledge is requied to have a better understanding.
- [Git](https://git-scm.com/)
- [Helm Charts](https://github.com/bitnami/charts)
- [GitHub Actions](https://docs.github.com/en/actions)

# Usage Instructions
1. `app_name` variable needs to be set from GitHub Console under below: 
```yaml
   Settings --> Secrets and Variables --> Actions --> Variables Tab.
```
2. Click on `New Repository Variable` and set variable name as per your wish. Here I've set `app_name`.
3. Now login with github cli - 
```yaml 
   gh auth login
```
4. Call the helm chart generator - 
```yaml
   gh workflow run "trigger helm chart generator"
```