# Branch Protection Settings for Main Branch

## Branch: main

### Protection Rules:
- ✅ Require pull request reviews before merging
- ✅ Require status checks to pass before merging  
- ✅ Require conversation resolution before merging
- ✅ Include administrators
- ✅ Restrict who can dismiss reviews

### Required Status Checks:
- ✅ **Python CI** - Matrix testing on all platforms
- ✅ **Docker CI** - Docker image build and push
- ✅ **Helm CI** - Helm chart packaging and validation

### Workflow Requirements:
- All CI jobs must pass before merge
- No direct pushes to main branch
- PR reviews required from code owners
- Status checks must be up-to-date before merge

### Environment Protections:
- **development**: Automated deployment after CI pass
- **staging**: Manual approval required for deployment