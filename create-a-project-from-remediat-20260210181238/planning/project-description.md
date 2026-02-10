# Azure Remediation Project Guide

## Project Type

This is an **Azure Remediation** project designed to address infrastructure issues, security vulnerabilities, and operational recommendations for [not specified].

## What This Project Will Do

### Phase 1: Issue Discovery
- Connect to vBox task 1237 in organization 9535197a-64b8-4ba6-b441-c31dadbe4676
- Retrieve remediation recommendations from vBox
- Analyze security, compliance, and operational issues
- Categorize issues by severity and impact
- Review affected resources and dependencies

### Phase 2: Remediation Planning
- Prioritize issues based on risk and business impact
- Assess remediation complexity and resource requirements
- Document prerequisites and dependencies
- Identify potential conflicts or rollback needs
- Create detailed remediation timeline

### Phase 3: Script Generation & Implementation
- Generate PowerShell remediation scripts for each issue
- Create runbook documentation for manual steps
- Provide testing and validation procedures
- Generate rollback scripts for safe deployment
- Track remediation progress and verify fixes

## Artifacts That Will Be Generated

| Artifact | Description | Location |
|----------|-------------|----------|
| Objective | Project goals and issue scope | `/objective.md` |
| Plan | Remediation plan and timeline | `/planning/plan.md` |
| Issue List | Detailed list of issues to remediate | `/analysis/issues.md` |
| Scripts | PowerShell remediation scripts | `/scripts/*.ps1` |
| Rollback Scripts | Emergency rollback procedures | `/scripts/rollback/*.ps1` |
| Runbook | Step-by-step remediation guide | `/documentation/runbook.md` |
| Test Plans | Validation and testing procedures | `/documentation/test-plan.md` |

## How to Interact With the Agent

### Example Prompts

**During Discovery Phase:**
- "Show me all remediation recommendations from vBox"
- "Which issues are high priority?"
- "Explain the security vulnerability in [resource name]"
- "What are the compliance issues found?"
- "Show me issues grouped by resource type"

**During Planning Phase:**
- "Prioritize issues by risk level"
- "What dependencies exist for fixing [issue ID]?"
- "Estimate the remediation effort for top 5 issues"
- "Create a phased remediation plan"
- "What are the rollback considerations?"

**During Implementation Phase:**
- "Generate a remediation script for issue #3"
- "Create a runbook for manual remediation steps"
- "Generate a rollback script for [resource name]"
- "Update the remediation progress tracker"
- "Validate that issue [xyz] has been fixed"
- "Show me remaining open issues"

### Next Steps

1. **Review Issues**: Ask the agent to show you all remediation recommendations
2. **Assess Impact**: Work with the agent to understand severity and business impact
3. **Plan Remediation**: Create a phased approach prioritizing critical issues
4. **Generate Scripts**: Request PowerShell scripts for automated remediation
5. **Test & Validate**: Use agent-generated test plans to verify fixes
6. **Track Progress**: Monitor remediation completion and document lessons learned

## Need Help?

Ask the agent:
- "What should I do next?"
- "Show me the remediation status"
- "What scripts have been generated?"
- "Explain issue [ID] in detail"
- "What's the current progress?"
- "Are there any blockers?"

## Project Context

- **vBox Task ID**: 1237
- **Organization**: 9535197a-64b8-4ba6-b441-c31dadbe4676
- **Customer**: [not specified]
