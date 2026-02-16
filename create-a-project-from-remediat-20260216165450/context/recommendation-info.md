# Task Information

## Overview
- **Customer**: Premier Medical
- **Task ID**: 469
- **Organization ID**: 996cacdf-f300-4332-ae85-416fcae15553

## Task Details
**Delete orphaned resources**


<br/><b><i>##- Please type your reply above this line -##</i></b><br/>
<h1>Please apply savings strategy below to optimize cost of attached azure resources</h1><p></p>
<h2><a href="https://portal.vbox-cloud.com/cost/optimization/details/ORO?clientId=996cacdf-f300-4332-ae85-416fcae15553" target="_blank">Delete orphaned resources</a></h2>
<p><p>When working with Azure, you can accidentally retain some unused data and resources. This can occur, for example, when you have disks connected to a VM with no workload assigned, or when you deploy test resources and then don&prime;t use them at all. We suggest removing these types of resources as they are useless.</p>
<p></p>
<h2>Strategy</h2>
<p><p>Analyze the metrics of all resources to find unused ones. If the metrics for a resource is 0, it may be an orphaned resource, so consider removing it.</p></p>

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
            <td>Garnet Bay Development</td>
             <td>6</td>
             <td>$1,007.31</td>
             <td>$0.00</td>
             <td>$1,007.31</td>
             <td>100.00%</td>
             <td>0.55%</td>
        </tr>
        <tr>
            <td>Dusk Trading Production</td>
             <td>4</td>
             <td>$2,116.97</td>
             <td>$0.00</td>
             <td>$2,116.97</td>
             <td>100.00%</td>
             <td>1.15%</td>
        </tr></tbody>
        <tfoot>
        <tr>
        <td><b>TOTAL:</b></td>
        <td><b>Monthly</b></td>
        <td>
            $3,124.29
        </td>
        <td>
            $0.00
        </td>
        <td>
            $3,124.29
        </td>
           <td>
            100.00%
        </td>
           <td>
            1.70%
        </td>
        </tr>
        <tr>
        <td></td>
        <td><b>Annually</b></td>
         <td>
            $37,491.44
        </td>
        <td>
            $0.00
        </td>
        <td>
            $37,491.44
        </td>
        </tr>
        </tfoot>
        </table>
<h2>Recommendations</h2>
<ul><li>Review service utilization to ensure it is properly used. Remove orphaned one.</li></ul>
<p><h2><a href="https://portal.vbox-cloud.com/cost/optimization/details/ORO?clientId=996cacdf-f300-4332-ae85-416fcae15553">View Details</a></h2></p>

## Recommendation
**Delete orphaned resources**

If a resource has no workload assigned to it and it costs money, we can remove it.

## Affected Resources
- **toolbox-search** (microsoft.search/searchservices)
  - Action: Delete resource
  - ID: `/subscriptions/ef6ab9ee-c114-4a57-9fc5-3082bbc5c914/resourcegroups/toolbox/providers/microsoft.search/searchservices/toolbox-search`
- **azr-dev2-sqldb/mudworks analytics** (microsoft.sql/servers/databases)
  - Action: Delete resource
  - ID: `/subscriptions/ef6ab9ee-c114-4a57-9fc5-3082bbc5c914/resourcegroups/defaultresourcegroup-ncus/providers/microsoft.sql/servers/azr-dev2-sqldb/databases/mudworks analytics`

## Remediation Steps
*No remediation steps provided*

---
*This document was auto-generated from vBox task data.*
