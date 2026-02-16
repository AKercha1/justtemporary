# Remediation Runbook - A. Datum Corporation

## Task: Downscale or shutdown Virtual Machines

## Recommendation
Downscale or shutdown Virtual Machines

## Affected Resources
- **dev-elderberry** (microsoft.compute/virtualmachines)
  - Action: Change from 'Standard_E8bds_v5' to 'Standard_E4bds_v5'
  - ID: `/subscriptions/5bd14da6-65ef-41c8-88ce-663170a1d6ff/resourcegroups/wcus-dev-pmd-vm01/providers/microsoft.compute/virtualmachines/dev-elderberry`
- **apple** (microsoft.compute/virtualmachines)
  - Action: Change from 'Standard_E8bds_v5' to 'Standard_E4bds_v5'
  - ID: `/subscriptions/5bd14da6-65ef-41c8-88ce-663170a1d6ff/resourcegroups/rg-wcus-p-compute-01/providers/microsoft.compute/virtualmachines/apple`
- **mrtdapp-reports** (microsoft.compute/virtualmachines)
  - Action: Change from 'Standard_D4ds_v5' to 'Standard_D4ads_v5'
  - ID: `/subscriptions/5bd14da6-65ef-41c8-88ce-663170a1d6ff/resourcegroups/rg-wcus-a-compute-01/providers/microsoft.compute/virtualmachines/mrtdapp-reports`
- **dld** (microsoft.compute/virtualmachines)
  - Action: Change from 'Standard_D4ds_v5' to 'Standard_D4ads_v5'
  - ID: `/subscriptions/5bd14da6-65ef-41c8-88ce-663170a1d6ff/resourcegroups/rg-wcus-a-compute-01/providers/microsoft.compute/virtualmachines/dld`
- **dapp-reports** (microsoft.compute/virtualmachines)
  - Action: Change from 'Standard_D4ds_v5' to 'Standard_D4ads_v5'
  - ID: `/subscriptions/5bd14da6-65ef-41c8-88ce-663170a1d6ff/resourcegroups/rg-wcus-a-compute-01/providers/microsoft.compute/virtualmachines/dapp-reports`
- **vmwcushapps01** (microsoft.compute/virtualmachines)
  - Action: Change from 'Standard_D4s_v3' to 'Standard_E2ads_v5'
  - ID: `/subscriptions/5bd14da6-65ef-41c8-88ce-663170a1d6ff/resourcegroups/rg-wcus-p-compute-01/providers/microsoft.compute/virtualmachines/vmwcushapps01`
- **iasandbox** (microsoft.compute/virtualmachines)
  - Action: Change from 'Standard_E8as_v5' to 'Standard_E4as_v5'
  - ID: `/subscriptions/5bd14da6-65ef-41c8-88ce-663170a1d6ff/resourcegroups/rg-wcus-d-compute-01/providers/microsoft.compute/virtualmachines/iasandbox`
- **alps** (microsoft.compute/virtualmachines)
  - Action: Change from 'Standard_E32ds_v5' to 'Standard_E32ads_v5'
  - ID: `/subscriptions/348c3a20-66f6-421a-b21c-97bb55449b11/resourcegroups/meriteuprod/providers/microsoft.compute/virtualmachines/alps`

## Pre-Execution Checklist

- [ ] Reviewed affected resources
- [ ] Generated remediation script
- [ ] Reviewed script parameters
- [ ] Obtained customer approval
- [ ] Scheduled execution window

## Execution Steps

*No remediation steps provided*

## Generated Scripts

| Script | Purpose | Status |
|--------|---------|--------|
| *(scripts will be listed here)* | | |

## Execution Results

### Successful Operations
*(to be documented after execution)*

### Failed Operations
*(to be documented after execution)*

## Post-Execution

- [ ] Verified remediation success
- [ ] Documented any issues
- [ ] Updated task status in vBox
- [ ] Customer sign-off obtained

---
*Last updated: {{date}}*
