# Task Information

## Overview
- **Customer**: A. Datum Corporation
- **Task ID**: 1313
- **Organization ID**: 9535197a-64b8-4ba6-b441-c31dadbe4676

## Task Details
**Downscale or shutdown Virtual Machines**


<br/><b><i>##- Please type your reply above this line -##</i></b><br/>
<h1>Please apply savings strategy below to optimize cost of attached azure resources</h1><p></p>
<h2><a href="https://portal-beta.vbox-cloud.com/organization/9535197a-64b8-4ba6-b441-c31dadbe4676/cost/optimization/details/VUT" target="_blank">Downscale or shutdown Virtual Machines</a></h2>
<p><p>Rightsizing is the process of analyzing the utilization and performance metrics of your infrastructure, determining whether it is running efficiently, and then modifying the infrastructure as needed.</p><p>In the scope of this optimization, we are rightsizing only VM compute.</p><p>Resizing your VMs and selecting the correct type can have a dramatic impact on your Azure costs. For example, even by going down one size within the same VM family, you can reduce costs by 50%. By making changes between families and/or other Azure VM sizes according to your region, you have the potential for even greater savings.</p>
<p></p>
<h2>Strategy</h2>
<p><h6>Shutdown recommendations</h6> <p>Advisor identifies resources that weren't used at all over the last seven days and makes a recommendation to shut them down.</p> <ul> <li>Recommendation criteria include <b>CPU</b> and <b>Outbound Network utilization metrics.</b> </li> <li>The last seven days of utilization data are analyzed.</li> <li>Metrics are sampled every 30 seconds, aggregated to 1 min and then further aggregated to 30 mins (we take the max of average values while aggregating to 30 mins).</li> <li>A shutdown recommendation is created if: <ul><li>P95 of the maximum value of CPU utilization summed across all cores is less than 3%</li> <li>P100 of average CPU in last 3 days (sum over all cores) is less that or equal 2%</li> <li>Outbound Network utilization is less than 2% over a seven-day period</li> </ul> </li> </ul> <h6>Resize SKU recommendations</h6> <p>We recommends resizing virtual machines when it's possible to fit the current load on a more appropriate SKU, which is less expensive (based on retail rates)</p> <ul> <li>Recommendation criteria include <b>CPU</b>, <b>Memory</b> and <b>Outbound Network utilization</b>.</li> <li>The last seven days of utilization data are analyzed.</li> <li>Metrics are sampled every 30 seconds, aggregated to 1 min and then further aggregated to 30 mins (we take the max of average values while aggregating to 30 mins).</li> <li>An appropriate SKU for virtual machines is determined based on the following criteria: <ul> <li>Target for user-facing workloads: <ul> <li>P95 of CPU and Outbound Network utilization at 40% or lower on the recommended SKU</li> <li>P100 of Memory utilization at 60% or lower on the recommended SKU</li> </ul> </li> <li>Target for non user-facing workloads: <ul> <li>P95 of the CPU and Outbound Network utilization at 80% or lower on the new SKU</li> <li>P100 of Memory utilization at 80% or lower on the new SKU</li> </ul> </li> </ul> </li> </ul> <h6>Burstable recommendations</h6> <p>A burstable SKU recommendation is made if:</p> <ul> <li>The average <b>CPU utilization</b> is less than a burstable SKUs' baseline performance <ul> <li>If the P95 of CPU is less than two times the burstable SKUs' baseline performance</li> <li>If the current SKU doesn't have accelerated networking enabled, since burstable SKUs don't support accelerated networking yet</li> <li>If we determine that the Burstable SKU credits are sufficient to support the average CPU utilization over 7 days.</li></ul></li> </ul></p>

        <h2>Estimated Cost Reduction</h2>
        <table>
         <tr>
           <td><strong>Name</strong></td>
           <td><strong>Unhealthy resources</strong></td>
           <td><strong>Current cost, $</strong></td>
           <td><strong>Optimized cost, $</strong></td>
           <td><strong>Saving, $</strong></td>
           <td><strong>Savings/Cost, %</strong></td>
           <td><strong>Savings/Total, %</strong></td>
        </tr>
        <tbody>
        <tr>
            <td>Azure</td>
             <td>7</td>
             <td>$3,626.64</td>
             <td>$2,280.24</td>
             <td>$1,346.40</td>
             <td>37.13%</td>
             <td>0.81%</td>
        </tr>
        <tr>
            <td>Azure EU</td>
             <td>1</td>
             <td>$3,006.72</td>
             <td>$2,822.40</td>
             <td>$184.32</td>
             <td>6.13%</td>
             <td>0.11%</td>
        </tr></tbody>
        <tfoot>
        <tr>
        <td><b>TOTAL:</b></td>
        <td><b>Monthly</b></td>
        <td>
            $6,633.36
        </td>
        <td>
            $5,102.64
        </td>
        <td>
            $1,530.72
        </td>
           <td>
            23.08%
        </td>
           <td>
            0.92%
        </td>
        </tr>
        <tr>
        <td></td>
        <td><b>Annually</b></td>
         <td>
            $79,600.32
        </td>
        <td>
            $61,231.68
        </td>
        <td>
            $18,368.64
        </td>
        </tr>
        </tfoot>
        </table>
<h2>Recommendations</h2>
<ul><li>Consider changing VMs tier.</li></ul>
<p><h2><a href="https://portal-beta.vbox-cloud.com/organization/9535197a-64b8-4ba6-b441-c31dadbe4676/cost/optimization/details/VUT">View Details</a></h2></p>

## Recommendation
**Downscale or shutdown Virtual Machines**

Select the appropriate size VM by analyzing the performance metrics to drastically decrease costs.

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

## Remediation Steps
*No remediation steps provided*

---
*This document was auto-generated from vBox task data.*
