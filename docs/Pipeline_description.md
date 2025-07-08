The CI/CD pipeline is defined using CircleCI and ensures that code quality and deployment are automated and repeatable.

## Workflow Steps
1. **Trigger**
   - Triggered on every push to the master branch.
2. **Build Job**
    - Install dependencies for frontend and backend.
    - Run lint and build scripts.
    - Fail-fast for errors or warnings.
3. **Hold Job**
   - Manual approval required before deploying to production.
4. **Deploy Job**
- Frontend:
    - Runs npm install and npm run build in udagram-frontend.
    - Deploys to AWS S3 using bin/deploy.sh.
- Backend:
    - Runs npm run deploy in udagram-api.
    - Deploys to AWS Elastic Beanstalk using EB CLI.

## Secrets Management
- CircleCI project settings store environment variables (e.g., DB credentials, JWT secrets).
- These variables are injected securely during build and deploy steps.
