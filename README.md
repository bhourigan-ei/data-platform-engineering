# data-platform-engineering


# To deploy and test:

## Fork this repository

## Configure branch protection

 1. Create GitHub repository secret ADMIN_TOKEN
 2. Generate a Personal Access Token with 'repo' permissions
 3. Add it to repository secrets
 4. Run workflow:
 - Go to Actions tab
 - Select "Configure Branch Protection" workflow
 - Click "Run workflow"
 - Select branch main
 - Click "Run workflow"

 5. Verify:
 - Go to Settings > Branches
 - Check protection rules for main and dev

## Configure Databricks Secrets

Add your GitHub repository:
```
DATABRICKS_TOKEN
DATABRICKS_HOST
SERVICE_PRINCIPAL_KEY
```

## Testing Feature Development
1. Create feature branch
2. Make changes either by:
    - logging into the databricks environment and make a simple change to the codebase.
    - make a change to the codebase on your local machine.
    - make a change in the feature branch codebase in the github repository itself (not recommended).
3. Push to trigger sync workflow
4. Create PR to dev to trigger tests


## Testing Deployment

1. Merge PR to dev to trigger development deployment
2. Create release tag to trigger pre-release deployment
3. Approve PR to main for production deployment