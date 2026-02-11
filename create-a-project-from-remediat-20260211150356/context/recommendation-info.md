# Task Information

## Overview
- **Customer**: A. Datum Corporation
- **Task ID**: 1237
- **Organization ID**: 9535197a-64b8-4ba6-b441-c31dadbe4676

## Task Details
**Downscale disks**


<br/><b><i>##- Please type your reply above this line -##</i></b><br/>
<h1>Please apply savings strategy below to optimize cost of attached azure resources</h1><p></p>
<h2><a href="https://portal-beta.vbox-cloud.com/organization/9535197a-64b8-4ba6-b441-c31dadbe4676/cost/optimization/details/DUT" target="_blank">Downscale disks</a></h2>
<p><p>There are 4 types of disks: HDD, SSD, premium SSD, and ultra disks. Each type is defined by performance and size constraints. In selecting an appropriate disk size, it is important to consider multiple factors, such as disk queue, IOPS, and throughput.</p><ul><li>Ultra disks<br/>Azure ultra disks are the highest-performing storage option for Azure VMs. You can change the performance parameters of an ultra disk without having to restart your VMs. Ultra disks are suited for data-intensive workloads and are therefore appropriate for SAP HANA, top-tier databases, and transaction-heavy workloads. Ultra disks must be used as data disks and can only be created as empty disks.</li><li>Premium SSDs<br/>Azure premium SSDs deliver high-performance and low-latency disk support for VMs with input/output-intensive workloads. Premium SSDs are suitable for mission-critical production applications, but you can use them only with compatible VM series.</li><li>Standard SSDs<br/>Azure standard SSDs are optimized for workloads that need consistent performance at lower IOPS levels. They&prime;re an especially good choice for varying workloads supported by on-premises HDD solutions. Compared to standard HDDs, standard SSDs deliver better availability, consistency, reliability, and latency. Standard SSDs are suitable for web servers, low IOPS application servers, lightly used enterprise applications, and non-production workloads. Like standard HDDs, standard SSDs are available on all Azure VMs.</li><li>Standard HDDs<br/>Azure standard HDDs deliver reliable, low-cost disk support for VMs running latency-tolerant workloads. With standard storage, your data is stored on HDDs, and performance may vary more widely than with SSD-based disks. When working with VMs, you can use standard HDD disks for dev/test scenarios and less-critical workloads.</li></ul>
<p></p>
<h2>Strategy</h2>
<p><p>Convert premium SSDs to standard SSDs for virtual servers with the following performance metrics:</p><table><thead><tr><th>Name</th><th>Limit</th></tr></thead><tbody><tr><td>OS Disk Queue Depth</td><td>&lt;= 1</td></tr><tr><td>OS per Disk Read Operations/Sec</td><td>&lt;= 500</td></tr><tr><td>OS per Disk Write Operations/Sec</td><td>&lt;= 500</td></tr><tr><td>OS Disk Read MBytes/Sec</td><td>&lt;= 50</td></tr><tr><td>OS Disk Write MBytes/Sec</td><td>&lt;= 50</td></tr></tbody></table><p>Note: To further investigate the applicability of this recommendation, VM Insights must be enabled on the selected set of VMs to collect disk-related Windows performance metrics.</p></p>

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
             <td>135</td>
             <td>$18,772.55</td>
             <td>$12,829.76</td>
             <td>$5,942.79</td>
             <td>31.66%</td>
             <td>3.69%</td>
        </tr>
        <tr>
            <td>Azure EU</td>
             <td>22</td>
             <td>$2,812.85</td>
             <td>$1,416.07</td>
             <td>$1,396.78</td>
             <td>49.66%</td>
             <td>0.87%</td>
        </tr></tbody>
        <tfoot>
        <tr>
        <td><b>TOTAL:</b></td>
        <td><b>Monthly</b></td>
        <td>
            $21,585.40
        </td>
        <td>
            $14,245.83
        </td>
        <td>
            $7,339.58
        </td>
           <td>
            34.00%
        </td>
           <td>
            4.55%
        </td>
        </tr>
        <tr>
        <td></td>
        <td><b>Annually</b></td>
         <td>
            $259,024.83
        </td>
        <td>
            $170,949.92
        </td>
        <td>
            $88,074.91
        </td>
        </tr>
        </tfoot>
        </table>
<h2>Recommendations</h2>
<ul><li>Enable Azure VM Insights data collection for 2 weeks and analyze performance.</li><li>Change disk type from Premium SSD to Standard SSD.</li></ul>
<p><h2><a href="https://portal-beta.vbox-cloud.com/organization/9535197a-64b8-4ba6-b441-c31dadbe4676/cost/optimization/details/DUT">View Details</a></h2></p>

## Recommendation
**Downscale disks**

Select the appropriate type of disk by analyzing the VM Insights statistics of disk-related Windows performance counters.

## Affected Resources
- **datamart2az-p30stripe6** (microsoft.compute/disks)
  - Action: Change tier from 'P50 LRS Disk' to 'E50 LRS Disk'
  - ID: `/subscriptions/5bd14da6-65ef-41c8-88ce-663170a1d6ff/resourcegroups/rg-wcus-p-compute-01/providers/microsoft.compute/disks/datamart2az-p30stripe6`
- **whs-adf-shire02_osdisk** (microsoft.compute/disks)
  - Action: Change tier from 'P10 LRS Disk' to 'E10 LRS Disk'
  - ID: `/subscriptions/5bd14da6-65ef-41c8-88ce-663170a1d6ff/resourcegroups/wcus-prod-it-shire-rg01/providers/microsoft.compute/disks/whs-adf-shire02_osdisk`
- **vmwcusdappgwcon_osdisk_1_15269101ca304db4bdad18414bafb2c0** (microsoft.compute/disks)
  - Action: Change tier from 'P10 LRS Disk' to 'E10 LRS Disk'
  - ID: `/subscriptions/5bd14da6-65ef-41c8-88ce-663170a1d6ff/resourcegroups/rg-wcus-d-compute-01/providers/microsoft.compute/disks/vmwcusdappgwcon_osdisk_1_15269101ca304db4bdad18414bafb2c0`
- **anteriadfwprod-osdisk** (microsoft.compute/disks)
  - Action: Change tier from 'P3 LRS Disk' to 'E3 LRS Disk'
  - ID: `/subscriptions/5bd14da6-65ef-41c8-88ce-663170a1d6ff/resourcegroups/anteriadfwprod/providers/microsoft.compute/disks/anteriadfwprod-osdisk`
- **mrtdapp-reports-osdisk-00** (microsoft.compute/disks)
  - Action: Change tier from 'P10 LRS Disk' to 'E10 LRS Disk'
  - ID: `/subscriptions/5bd14da6-65ef-41c8-88ce-663170a1d6ff/resourcegroups/rg-wcus-a-compute-01/providers/microsoft.compute/disks/mrtdapp-reports-osdisk-00`
- **mrtweb2-osdisk-00** (microsoft.compute/disks)
  - Action: Change tier from 'P30 LRS Disk' to 'E30 LRS Disk'
  - ID: `/subscriptions/5bd14da6-65ef-41c8-88ce-663170a1d6ff/resourcegroups/rg-wcus-a-compute-01/providers/microsoft.compute/disks/mrtweb2-osdisk-00`
- **vmwcushnetutil_osdisk** (microsoft.compute/disks)
  - Action: Change tier from 'P10 LRS Disk' to 'E10 LRS Disk'
  - ID: `/subscriptions/5bd14da6-65ef-41c8-88ce-663170a1d6ff/resourcegroups/rg-wcus-h-compute-01/providers/microsoft.compute/disks/vmwcushnetutil_osdisk`
- **birch_osdisk** (microsoft.compute/disks)
  - Action: Change tier from 'P10 LRS Disk' to 'E10 LRS Disk'
  - ID: `/subscriptions/5bd14da6-65ef-41c8-88ce-663170a1d6ff/resourcegroups/rg-wcus-p-compute-01/providers/microsoft.compute/disks/birch_osdisk`
- **ia-adf-shire01_osdisk** (microsoft.compute/disks)
  - Action: Change tier from 'P10 LRS Disk' to 'S10 LRS Disk'
  - ID: `/subscriptions/5bd14da6-65ef-41c8-88ce-663170a1d6ff/resourcegroups/wcus-prod-it-shire-rg01/providers/microsoft.compute/disks/ia-adf-shire01_osdisk`
- **pmd-adf-shire01_osdisk** (microsoft.compute/disks)
  - Action: Change tier from 'P10 LRS Disk' to 'E10 LRS Disk'
  - ID: `/subscriptions/5bd14da6-65ef-41c8-88ce-663170a1d6ff/resourcegroups/wcus-prod-it-shire-rg01/providers/microsoft.compute/disks/pmd-adf-shire01_osdisk`
- **vmwcusdba01_osdisk** (microsoft.compute/disks)
  - Action: Change tier from 'P10 LRS Disk' to 'E10 LRS Disk'
  - ID: `/subscriptions/5bd14da6-65ef-41c8-88ce-663170a1d6ff/resourcegroups/wcus-prod-dba-core-rg01/providers/microsoft.compute/disks/vmwcusdba01_osdisk`
- **ia-prod-domo01_osdisk** (microsoft.compute/disks)
  - Action: Change tier from 'P10 LRS Disk' to 'S10 LRS Disk'
  - ID: `/subscriptions/5bd14da6-65ef-41c8-88ce-663170a1d6ff/resourcegroups/wcus-prod-ia-core-rg01/providers/microsoft.compute/disks/ia-prod-domo01_osdisk`
- **cmd-adf-shire01_osdisk** (microsoft.compute/disks)
  - Action: Change tier from 'P10 LRS Disk' to 'E10 LRS Disk'
  - ID: `/subscriptions/5bd14da6-65ef-41c8-88ce-663170a1d6ff/resourcegroups/wcus-prod-it-shire-rg01/providers/microsoft.compute/disks/cmd-adf-shire01_osdisk`
- **vmwcushmdca_osdisk** (microsoft.compute/disks)
  - Action: Change tier from 'P10 LRS Disk' to 'E10 LRS Disk'
  - ID: `/subscriptions/5bd14da6-65ef-41c8-88ce-663170a1d6ff/resourcegroups/rg-wcus-h-compute-01/providers/microsoft.compute/disks/vmwcushmdca_osdisk`
- **vmwcushmddc02_osdisk_1_9e16b1fb917b4949a6004dfd98303017** (microsoft.compute/disks)
  - Action: Change tier from 'P10 LRS Disk' to 'E10 LRS Disk'
  - ID: `/subscriptions/5bd14da6-65ef-41c8-88ce-663170a1d6ff/resourcegroups/rg-wcus-h-compute-01/providers/microsoft.compute/disks/vmwcushmddc02_osdisk_1_9e16b1fb917b4949a6004dfd98303017`
- **vmwcushnetdc001_osdisk_1_91d7c717c5e54368a67e522bbaa3410a** (microsoft.compute/disks)
  - Action: Change tier from 'P10 LRS Disk' to 'E10 LRS Disk'
  - ID: `/subscriptions/5bd14da6-65ef-41c8-88ce-663170a1d6ff/resourcegroups/rg-wcus-h-compute-01/providers/microsoft.compute/disks/vmwcushnetdc001_osdisk_1_91d7c717c5e54368a67e522bbaa3410a`
- **vmwcushnetdc002_disk1_502837afd400416683f6f466b2ff8164** (microsoft.compute/disks)
  - Action: Change tier from 'P10 LRS Disk' to 'S10 LRS Disk'
  - ID: `/subscriptions/5bd14da6-65ef-41c8-88ce-663170a1d6ff/resourcegroups/rg-wcus-h-compute-01/providers/microsoft.compute/disks/vmwcushnetdc002_disk1_502837afd400416683f6f466b2ff8164`
- **vmwcushdmzdc001_disk1_b75f8c96de0844afbf0d05bc6af09e4a** (microsoft.compute/disks)
  - Action: Change tier from 'P10 LRS Disk' to 'E10 LRS Disk'
  - ID: `/subscriptions/5bd14da6-65ef-41c8-88ce-663170a1d6ff/resourcegroups/rg-wcus-h-compute-01/providers/microsoft.compute/disks/vmwcushdmzdc001_disk1_b75f8c96de0844afbf0d05bc6af09e4a`
- **vmwcushdmzdc002_disk1_209a74399d724b7cb646a6c31c3251c0** (microsoft.compute/disks)
  - Action: Change tier from 'P10 LRS Disk' to 'S10 LRS Disk'
  - ID: `/subscriptions/5bd14da6-65ef-41c8-88ce-663170a1d6ff/resourcegroups/rg-wcus-h-compute-01/providers/microsoft.compute/disks/vmwcushdmzdc002_disk1_209a74399d724b7cb646a6c31c3251c0`
- **itadfshire01-osdisk-20251227-065209** (microsoft.compute/disks)
  - Action: Change tier from 'P10 LRS Disk' to 'E10 LRS Disk'
  - ID: `/subscriptions/5bd14da6-65ef-41c8-88ce-663170a1d6ff/resourcegroups/wcus-prod-it-shire-rg01/providers/microsoft.compute/disks/itadfshire01-osdisk-20251227-065209`
- **iasynshire01-osdisk-20251227-082056** (microsoft.compute/disks)
  - Action: Change tier from 'P10 LRS Disk' to 'E10 LRS Disk'
  - ID: `/subscriptions/5bd14da6-65ef-41c8-88ce-663170a1d6ff/resourcegroups/wcus-prod-it-shire-rg01/providers/microsoft.compute/disks/iasynshire01-osdisk-20251227-082056`
- **vmwcushdmzdc01res-osdisk-20251227-091706** (microsoft.compute/disks)
  - Action: Change tier from 'P10 LRS Disk' to 'S10 LRS Disk'
  - ID: `/subscriptions/5bd14da6-65ef-41c8-88ce-663170a1d6ff/resourcegroups/rg-wcus-h-compute-01/providers/microsoft.compute/disks/vmwcushdmzdc01res-osdisk-20251227-091706`
- **vmwcushdmzdc02res-osdisk-20251227-091744** (microsoft.compute/disks)
  - Action: Change tier from 'P10 LRS Disk' to 'E10 LRS Disk'
  - ID: `/subscriptions/5bd14da6-65ef-41c8-88ce-663170a1d6ff/resourcegroups/rg-wcus-h-compute-01/providers/microsoft.compute/disks/vmwcushdmzdc02res-osdisk-20251227-091744`
- **mdchfs02res-osdisk-20251228-223226** (microsoft.compute/disks)
  - Action: Change tier from 'P15 LRS Disk' to 'E15 LRS Disk'
  - ID: `/subscriptions/5bd14da6-65ef-41c8-88ce-663170a1d6ff/resourcegroups/rg-wcus-p-compute-01/providers/microsoft.compute/disks/mdchfs02res-osdisk-20251228-223226`
- **ia-adf-shire02_osdisk** (microsoft.compute/disks)
  - Action: Change tier from 'P10 LRS Disk' to 'S10 LRS Disk'
  - ID: `/subscriptions/5bd14da6-65ef-41c8-88ce-663170a1d6ff/resourcegroups/wcus-prod-it-shire-rg01/providers/microsoft.compute/disks/ia-adf-shire02_osdisk`
- **anteastutil-osdisk-20251227-081936** (microsoft.compute/disks)
  - Action: Change tier from 'P10 LRS Disk' to 'S10 LRS Disk'
  - ID: `/subscriptions/5bd14da6-65ef-41c8-88ce-663170a1d6ff/resourcegroups/anteriadryebrookprod/providers/microsoft.compute/disks/anteastutil-osdisk-20251227-081936`
- **banyan_logs** (microsoft.compute/disks)
  - Action: Change tier from 'P50 LRS Disk' to 'E50 LRS Disk'
  - ID: `/subscriptions/5bd14da6-65ef-41c8-88ce-663170a1d6ff/resourcegroups/rg-wcus-p-compute-01/providers/microsoft.compute/disks/banyan_logs`
- **banyan_db** (microsoft.compute/disks)
  - Action: Change tier from 'P50 LRS Disk' to 'E50 LRS Disk'
  - ID: `/subscriptions/5bd14da6-65ef-41c8-88ce-663170a1d6ff/resourcegroups/rg-wcus-p-compute-01/providers/microsoft.compute/disks/banyan_db`
- **banyan_tempdb** (microsoft.compute/disks)
  - Action: Change tier from 'P50 LRS Disk' to 'E50 LRS Disk'
  - ID: `/subscriptions/5bd14da6-65ef-41c8-88ce-663170a1d6ff/resourcegroups/rg-wcus-p-compute-01/providers/microsoft.compute/disks/banyan_tempdb`
- **mango_dblogs** (microsoft.compute/disks)
  - Action: Change tier from 'P10 LRS Disk' to 'E10 LRS Disk'
  - ID: `/subscriptions/5bd14da6-65ef-41c8-88ce-663170a1d6ff/resourcegroups/rg-wcus-p-compute-01/providers/microsoft.compute/disks/mango_dblogs`
- **mango_databases** (microsoft.compute/disks)
  - Action: Change tier from 'P10 LRS Disk' to 'E10 LRS Disk'
  - ID: `/subscriptions/5bd14da6-65ef-41c8-88ce-663170a1d6ff/resourcegroups/rg-wcus-p-compute-01/providers/microsoft.compute/disks/mango_databases`
- **mango_files** (microsoft.compute/disks)
  - Action: Change tier from 'P10 LRS Disk' to 'E10 LRS Disk'
  - ID: `/subscriptions/5bd14da6-65ef-41c8-88ce-663170a1d6ff/resourcegroups/rg-wcus-p-compute-01/providers/microsoft.compute/disks/mango_files`
- **cottonwood-osdisk-00** (microsoft.compute/disks)
  - Action: Change tier from 'E15 LRS Disk' to 'S15 LRS Disk'
  - ID: `/subscriptions/5bd14da6-65ef-41c8-88ce-663170a1d6ff/resourcegroups/rg-wcus-d-compute-01/providers/microsoft.compute/disks/cottonwood-osdisk-00`
- **mango_tempdb** (microsoft.compute/disks)
  - Action: Change tier from 'P4 LRS Disk' to 'E4 LRS Disk'
  - ID: `/subscriptions/5bd14da6-65ef-41c8-88ce-663170a1d6ff/resourcegroups/rg-wcus-p-compute-01/providers/microsoft.compute/disks/mango_tempdb`
- **iasandbox_logs** (microsoft.compute/disks)
  - Action: Change tier from 'P40 LRS Disk' to 'E40 LRS Disk'
  - ID: `/subscriptions/5bd14da6-65ef-41c8-88ce-663170a1d6ff/resourcegroups/rg-wcus-d-compute-01/providers/microsoft.compute/disks/iasandbox_logs`
- **iasandbox_database1** (microsoft.compute/disks)
  - Action: Change tier from 'P50 LRS Disk' to 'E50 LRS Disk'
  - ID: `/subscriptions/5bd14da6-65ef-41c8-88ce-663170a1d6ff/resourcegroups/rg-wcus-d-compute-01/providers/microsoft.compute/disks/iasandbox_database1`
- **db12-osdisk-20231020-183654** (microsoft.compute/disks)
  - Action: Change tier from 'E10 LRS Disk' to 'S10 LRS Disk'
  - ID: `/subscriptions/5bd14da6-65ef-41c8-88ce-663170a1d6ff/resourcegroups/rg-wcus-d-compute-01/providers/microsoft.compute/disks/db12-osdisk-20231020-183654`
- **papaya_databases** (microsoft.compute/disks)
  - Action: Change tier from 'P40 LRS Disk' to 'E40 LRS Disk'
  - ID: `/subscriptions/5bd14da6-65ef-41c8-88ce-663170a1d6ff/resourcegroups/rg-wcus-p-compute-01/providers/microsoft.compute/disks/papaya_databases`
- **iasandbox_tempdb** (microsoft.compute/disks)
  - Action: Change tier from 'P30 LRS Disk' to 'E30 LRS Disk'
  - ID: `/subscriptions/5bd14da6-65ef-41c8-88ce-663170a1d6ff/resourcegroups/rg-wcus-d-compute-01/providers/microsoft.compute/disks/iasandbox_tempdb`
- **sal_logs** (microsoft.compute/disks)
  - Action: Change tier from 'P20 LRS Disk' to 'E20 LRS Disk'
  - ID: `/subscriptions/5bd14da6-65ef-41c8-88ce-663170a1d6ff/resourcegroups/rg-wcus-p-compute-01/providers/microsoft.compute/disks/sal_logs`
- **sal_tempdb** (microsoft.compute/disks)
  - Action: Change tier from 'P15 LRS Disk' to 'E15 LRS Disk'
  - ID: `/subscriptions/5bd14da6-65ef-41c8-88ce-663170a1d6ff/resourcegroups/rg-wcus-p-compute-01/providers/microsoft.compute/disks/sal_tempdb`
- **sal_files** (microsoft.compute/disks)
  - Action: Change tier from 'P10 LRS Disk' to 'E10 LRS Disk'
  - ID: `/subscriptions/5bd14da6-65ef-41c8-88ce-663170a1d6ff/resourcegroups/rg-wcus-p-compute-01/providers/microsoft.compute/disks/sal_files`
- **sal_db** (microsoft.compute/disks)
  - Action: Change tier from 'P30 LRS Disk' to 'E30 LRS Disk'
  - ID: `/subscriptions/5bd14da6-65ef-41c8-88ce-663170a1d6ff/resourcegroups/rg-wcus-p-compute-01/providers/microsoft.compute/disks/sal_db`
- **vmwcushapps01_datadisk_0** (microsoft.compute/disks)
  - Action: Change tier from 'P15 LRS Disk' to 'E15 LRS Disk'
  - ID: `/subscriptions/5bd14da6-65ef-41c8-88ce-663170a1d6ff/resourcegroups/rg-wcus-p-compute-01/providers/microsoft.compute/disks/vmwcushapps01_datadisk_0`
- **datamart2az-p30stripe3** (microsoft.compute/disks)
  - Action: Change tier from 'P50 LRS Disk' to 'E50 LRS Disk'
  - ID: `/subscriptions/5bd14da6-65ef-41c8-88ce-663170a1d6ff/resourcegroups/rg-wcus-p-compute-01/providers/microsoft.compute/disks/datamart2az-p30stripe3`
- **datamart2az-p30stripe1** (microsoft.compute/disks)
  - Action: Change tier from 'P50 LRS Disk' to 'E50 LRS Disk'
  - ID: `/subscriptions/5bd14da6-65ef-41c8-88ce-663170a1d6ff/resourcegroups/rg-wcus-p-compute-01/providers/microsoft.compute/disks/datamart2az-p30stripe1`
- **datamart2az-p30stripe2** (microsoft.compute/disks)
  - Action: Change tier from 'P50 LRS Disk' to 'E50 LRS Disk'
  - ID: `/subscriptions/5bd14da6-65ef-41c8-88ce-663170a1d6ff/resourcegroups/rg-wcus-p-compute-01/providers/microsoft.compute/disks/datamart2az-p30stripe2`
- **datamart2az-p30stripe10** (microsoft.compute/disks)
  - Action: Change tier from 'P50 LRS Disk' to 'E50 LRS Disk'
  - ID: `/subscriptions/5bd14da6-65ef-41c8-88ce-663170a1d6ff/resourcegroups/rg-wcus-p-compute-01/providers/microsoft.compute/disks/datamart2az-p30stripe10`
- **datamart2az-p30stripe5** (microsoft.compute/disks)
  - Action: Change tier from 'P50 LRS Disk' to 'E50 LRS Disk'
  - ID: `/subscriptions/5bd14da6-65ef-41c8-88ce-663170a1d6ff/resourcegroups/rg-wcus-p-compute-01/providers/microsoft.compute/disks/datamart2az-p30stripe5`
- **datamart2az-p30stripe7** (microsoft.compute/disks)
  - Action: Change tier from 'P50 LRS Disk' to 'E50 LRS Disk'
  - ID: `/subscriptions/5bd14da6-65ef-41c8-88ce-663170a1d6ff/resourcegroups/rg-wcus-p-compute-01/providers/microsoft.compute/disks/datamart2az-p30stripe7`
- **datamart2az-logs** (microsoft.compute/disks)
  - Action: Change tier from 'P50 LRS Disk' to 'E50 LRS Disk'
  - ID: `/subscriptions/5bd14da6-65ef-41c8-88ce-663170a1d6ff/resourcegroups/rg-wcus-p-compute-01/providers/microsoft.compute/disks/datamart2az-logs`
- **datamart2az-p30stripe4** (microsoft.compute/disks)
  - Action: Change tier from 'P50 LRS Disk' to 'E50 LRS Disk'
  - ID: `/subscriptions/5bd14da6-65ef-41c8-88ce-663170a1d6ff/resourcegroups/rg-wcus-p-compute-01/providers/microsoft.compute/disks/datamart2az-p30stripe4`
- **datamart2az-p30stripe8** (microsoft.compute/disks)
  - Action: Change tier from 'P50 LRS Disk' to 'E50 LRS Disk'
  - ID: `/subscriptions/5bd14da6-65ef-41c8-88ce-663170a1d6ff/resourcegroups/rg-wcus-p-compute-01/providers/microsoft.compute/disks/datamart2az-p30stripe8`
- **datamart2az-p30stripe9** (microsoft.compute/disks)
  - Action: Change tier from 'P50 LRS Disk' to 'E50 LRS Disk'
  - ID: `/subscriptions/5bd14da6-65ef-41c8-88ce-663170a1d6ff/resourcegroups/rg-wcus-p-compute-01/providers/microsoft.compute/disks/datamart2az-p30stripe9`
- **mrtdatamart2az_p50stripe2** (microsoft.compute/disks)
  - Action: Change tier from 'P50 LRS Disk' to 'E50 LRS Disk'
  - ID: `/subscriptions/5bd14da6-65ef-41c8-88ce-663170a1d6ff/resourcegroups/rg-wcus-p-compute-01/providers/microsoft.compute/disks/mrtdatamart2az_p50stripe2`
- **mrtdatamart2az_p50stripe3** (microsoft.compute/disks)
  - Action: Change tier from 'P50 LRS Disk' to 'E50 LRS Disk'
  - ID: `/subscriptions/5bd14da6-65ef-41c8-88ce-663170a1d6ff/resourcegroups/rg-wcus-p-compute-01/providers/microsoft.compute/disks/mrtdatamart2az_p50stripe3`
- **mrtdatamart2az_p50stripe7** (microsoft.compute/disks)
  - Action: Change tier from 'P50 LRS Disk' to 'E50 LRS Disk'
  - ID: `/subscriptions/5bd14da6-65ef-41c8-88ce-663170a1d6ff/resourcegroups/rg-wcus-p-compute-01/providers/microsoft.compute/disks/mrtdatamart2az_p50stripe7`
- **mrtdatamart2az_p50stripe4** (microsoft.compute/disks)
  - Action: Change tier from 'P50 LRS Disk' to 'E50 LRS Disk'
  - ID: `/subscriptions/5bd14da6-65ef-41c8-88ce-663170a1d6ff/resourcegroups/rg-wcus-p-compute-01/providers/microsoft.compute/disks/mrtdatamart2az_p50stripe4`
- **mrtdatamart2az_p50stripe5** (microsoft.compute/disks)
  - Action: Change tier from 'P50 LRS Disk' to 'E50 LRS Disk'
  - ID: `/subscriptions/5bd14da6-65ef-41c8-88ce-663170a1d6ff/resourcegroups/rg-wcus-p-compute-01/providers/microsoft.compute/disks/mrtdatamart2az_p50stripe5`
- **mrtdatamart2az_p50stripe6** (microsoft.compute/disks)
  - Action: Change tier from 'P50 LRS Disk' to 'E50 LRS Disk'
  - ID: `/subscriptions/5bd14da6-65ef-41c8-88ce-663170a1d6ff/resourcegroups/rg-wcus-p-compute-01/providers/microsoft.compute/disks/mrtdatamart2az_p50stripe6`
- **mrtdatamart2az_p50stripe8** (microsoft.compute/disks)
  - Action: Change tier from 'P50 LRS Disk' to 'E50 LRS Disk'
  - ID: `/subscriptions/5bd14da6-65ef-41c8-88ce-663170a1d6ff/resourcegroups/rg-wcus-p-compute-01/providers/microsoft.compute/disks/mrtdatamart2az_p50stripe8`
- **mrtdatamart2az_p50stripe1** (microsoft.compute/disks)
  - Action: Change tier from 'P50 LRS Disk' to 'E50 LRS Disk'
  - ID: `/subscriptions/5bd14da6-65ef-41c8-88ce-663170a1d6ff/resourcegroups/rg-wcus-p-compute-01/providers/microsoft.compute/disks/mrtdatamart2az_p50stripe1`
- **mrtdatamart2az_sqllog** (microsoft.compute/disks)
  - Action: Change tier from 'P30 LRS Disk' to 'E30 LRS Disk'
  - ID: `/subscriptions/5bd14da6-65ef-41c8-88ce-663170a1d6ff/resourcegroups/rg-wcus-p-compute-01/providers/microsoft.compute/disks/mrtdatamart2az_sqllog`
- **datamart2az-p30stripe12** (microsoft.compute/disks)
  - Action: Change tier from 'P50 LRS Disk' to 'E50 LRS Disk'
  - ID: `/subscriptions/5bd14da6-65ef-41c8-88ce-663170a1d6ff/resourcegroups/rg-wcus-p-compute-01/providers/microsoft.compute/disks/datamart2az-p30stripe12`
- **datamart2az-p30stripe13** (microsoft.compute/disks)
  - Action: Change tier from 'P50 LRS Disk' to 'E50 LRS Disk'
  - ID: `/subscriptions/5bd14da6-65ef-41c8-88ce-663170a1d6ff/resourcegroups/rg-wcus-p-compute-01/providers/microsoft.compute/disks/datamart2az-p30stripe13`
- **datamart2az-p30stripe14** (microsoft.compute/disks)
  - Action: Change tier from 'P50 LRS Disk' to 'E50 LRS Disk'
  - ID: `/subscriptions/5bd14da6-65ef-41c8-88ce-663170a1d6ff/resourcegroups/rg-wcus-p-compute-01/providers/microsoft.compute/disks/datamart2az-p30stripe14`
- **datamart2az-p30stripe16** (microsoft.compute/disks)
  - Action: Change tier from 'P50 LRS Disk' to 'E50 LRS Disk'
  - ID: `/subscriptions/5bd14da6-65ef-41c8-88ce-663170a1d6ff/resourcegroups/rg-wcus-p-compute-01/providers/microsoft.compute/disks/datamart2az-p30stripe16`
- **datamart2az-p30stripe11** (microsoft.compute/disks)
  - Action: Change tier from 'P50 LRS Disk' to 'E50 LRS Disk'
  - ID: `/subscriptions/5bd14da6-65ef-41c8-88ce-663170a1d6ff/resourcegroups/rg-wcus-p-compute-01/providers/microsoft.compute/disks/datamart2az-p30stripe11`
- **datamart2az-p30stripe15** (microsoft.compute/disks)
  - Action: Change tier from 'P50 LRS Disk' to 'E50 LRS Disk'
  - ID: `/subscriptions/5bd14da6-65ef-41c8-88ce-663170a1d6ff/resourcegroups/rg-wcus-p-compute-01/providers/microsoft.compute/disks/datamart2az-p30stripe15`
- **thomagata-pinnacledata** (microsoft.compute/disks)
  - Action: Change tier from 'P40 LRS Disk' to 'E40 LRS Disk'
  - ID: `/subscriptions/5bd14da6-65ef-41c8-88ce-663170a1d6ff/resourcegroups/rg-wcus-p-compute-01/providers/microsoft.compute/disks/thomagata-pinnacledata`
- **thomagata-mercurydata** (microsoft.compute/disks)
  - Action: Change tier from 'P60 LRS Disk' to 'E60 LRS Disk'
  - ID: `/subscriptions/5bd14da6-65ef-41c8-88ce-663170a1d6ff/resourcegroups/rg-wcus-p-compute-01/providers/microsoft.compute/disks/thomagata-mercurydata`
- **dev-elderberry_data01** (microsoft.compute/disks)
  - Action: Change tier from 'P40 LRS Disk' to 'E40 LRS Disk'
  - ID: `/subscriptions/5bd14da6-65ef-41c8-88ce-663170a1d6ff/resourcegroups/wcus-dev-pmd-vm01/providers/microsoft.compute/disks/dev-elderberry_data01`
- **mdfile02res-osdisk-20251227-081118** (microsoft.compute/disks)
  - Action: Change tier from 'E10 LRS Disk' to 'S10 LRS Disk'
  - ID: `/subscriptions/5bd14da6-65ef-41c8-88ce-663170a1d6ff/resourcegroups/anteriadryebrookprod/providers/microsoft.compute/disks/mdfile02res-osdisk-20251227-081118`
- **mrtdatamart1-dblog** (microsoft.compute/disks)
  - Action: Change tier from 'P30 LRS Disk' to 'E30 LRS Disk'
  - ID: `/subscriptions/5bd14da6-65ef-41c8-88ce-663170a1d6ff/resourcegroups/rg-wcus-p-compute-01/providers/microsoft.compute/disks/mrtdatamart1-dblog`
- **mrtdatamart1-dbp40** (microsoft.compute/disks)
  - Action: Change tier from 'P40 LRS Disk' to 'E40 LRS Disk'
  - ID: `/subscriptions/5bd14da6-65ef-41c8-88ce-663170a1d6ff/resourcegroups/rg-wcus-p-compute-01/providers/microsoft.compute/disks/mrtdatamart1-dbp40`
- **mrtdatamart1-dbp50** (microsoft.compute/disks)
  - Action: Change tier from 'P50 LRS Disk' to 'E50 LRS Disk'
  - ID: `/subscriptions/5bd14da6-65ef-41c8-88ce-663170a1d6ff/resourcegroups/rg-wcus-p-compute-01/providers/microsoft.compute/disks/mrtdatamart1-dbp50`
- **mrtdatamart1-dbp40-2** (microsoft.compute/disks)
  - Action: Change tier from 'P40 LRS Disk' to 'E40 LRS Disk'
  - ID: `/subscriptions/5bd14da6-65ef-41c8-88ce-663170a1d6ff/resourcegroups/rg-wcus-p-compute-01/providers/microsoft.compute/disks/mrtdatamart1-dbp40-2`
- **vmwcusvdi-whs_datadisk_0** (microsoft.compute/disks)
  - Action: Change tier from 'P30 LRS Disk' to 'E30 LRS Disk'
  - ID: `/subscriptions/5bd14da6-65ef-41c8-88ce-663170a1d6ff/resourcegroups/rg-wcus-p-compute-01/providers/microsoft.compute/disks/vmwcusvdi-whs_datadisk_0`
- **wcusdevitvm02-userlog** (microsoft.compute/disks)
  - Action: Change tier from 'P15 LRS Disk' to 'E15 LRS Disk'
  - ID: `/subscriptions/5bd14da6-65ef-41c8-88ce-663170a1d6ff/resourcegroups/rg-wcus-d-compute-01/providers/microsoft.compute/disks/wcusdevitvm02-userlog`
- **wcusdevitvm02-userdb** (microsoft.compute/disks)
  - Action: Change tier from 'P20 LRS Disk' to 'E20 LRS Disk'
  - ID: `/subscriptions/5bd14da6-65ef-41c8-88ce-663170a1d6ff/resourcegroups/rg-wcus-d-compute-01/providers/microsoft.compute/disks/wcusdevitvm02-userdb`
- **wcusdevitvm02-systemdb** (microsoft.compute/disks)
  - Action: Change tier from 'P10 LRS Disk' to 'E10 LRS Disk'
  - ID: `/subscriptions/5bd14da6-65ef-41c8-88ce-663170a1d6ff/resourcegroups/rg-wcus-d-compute-01/providers/microsoft.compute/disks/wcusdevitvm02-systemdb`
- **wcusdevitvm02-dpacentral** (microsoft.compute/disks)
  - Action: Change tier from 'P20 LRS Disk' to 'E20 LRS Disk'
  - ID: `/subscriptions/5bd14da6-65ef-41c8-88ce-663170a1d6ff/resourcegroups/rg-wcus-d-compute-01/providers/microsoft.compute/disks/wcusdevitvm02-dpacentral`
- **banyan_userdb_f** (microsoft.compute/disks)
  - Action: Change tier from 'P40 LRS Disk' to 'E40 LRS Disk'
  - ID: `/subscriptions/5bd14da6-65ef-41c8-88ce-663170a1d6ff/resourcegroups/rg-wcus-p-compute-01/providers/microsoft.compute/disks/banyan_userdb_f`
- **birch-systemdb** (microsoft.compute/disks)
  - Action: Change tier from 'P3 LRS Disk' to 'E3 LRS Disk'
  - ID: `/subscriptions/5bd14da6-65ef-41c8-88ce-663170a1d6ff/resourcegroups/rg-wcus-p-compute-01/providers/microsoft.compute/disks/birch-systemdb`
- **birch-dblogs01** (microsoft.compute/disks)
  - Action: Change tier from 'P30 LRS Disk' to 'E30 LRS Disk'
  - ID: `/subscriptions/5bd14da6-65ef-41c8-88ce-663170a1d6ff/resourcegroups/rg-wcus-p-compute-01/providers/microsoft.compute/disks/birch-dblogs01`
- **birch-dbdata01** (microsoft.compute/disks)
  - Action: Change tier from 'P40 LRS Disk' to 'E40 LRS Disk'
  - ID: `/subscriptions/5bd14da6-65ef-41c8-88ce-663170a1d6ff/resourcegroups/rg-wcus-p-compute-01/providers/microsoft.compute/disks/birch-dbdata01`
- **banyan_userdb_g** (microsoft.compute/disks)
  - Action: Change tier from 'P40 LRS Disk' to 'E40 LRS Disk'
  - ID: `/subscriptions/5bd14da6-65ef-41c8-88ce-663170a1d6ff/resourcegroups/rg-wcus-p-compute-01/providers/microsoft.compute/disks/banyan_userdb_g`
- **vmwcusdba01_systemdbs** (microsoft.compute/disks)
  - Action: Change tier from 'P1 LRS Disk' to 'E1 LRS Disk'
  - ID: `/subscriptions/5bd14da6-65ef-41c8-88ce-663170a1d6ff/resourcegroups/wcus-prod-dba-core-rg01/providers/microsoft.compute/disks/vmwcusdba01_systemdbs`
- **vmwcusdba01_userdbs** (microsoft.compute/disks)
  - Action: Change tier from 'P1 LRS Disk' to 'E1 LRS Disk'
  - ID: `/subscriptions/5bd14da6-65ef-41c8-88ce-663170a1d6ff/resourcegroups/wcus-prod-dba-core-rg01/providers/microsoft.compute/disks/vmwcusdba01_userdbs`
- **vmwcusdba01_userlogs** (microsoft.compute/disks)
  - Action: Change tier from 'P1 LRS Disk' to 'E1 LRS Disk'
  - ID: `/subscriptions/5bd14da6-65ef-41c8-88ce-663170a1d6ff/resourcegroups/wcus-prod-dba-core-rg01/providers/microsoft.compute/disks/vmwcusdba01_userlogs`
- **tigerwoodaz-datadisk-001-20260113-215044** (microsoft.compute/disks)
  - Action: Change tier from 'P40 LRS Disk' to 'E40 LRS Disk'
  - ID: `/subscriptions/5bd14da6-65ef-41c8-88ce-663170a1d6ff/resourcegroups/rg-wcus-p-compute-01/providers/microsoft.compute/disks/tigerwoodaz-datadisk-001-20260113-215044`
- **tigerwoodaz-datadisk-006-20260113-215044** (microsoft.compute/disks)
  - Action: Change tier from 'P40 LRS Disk' to 'E40 LRS Disk'
  - ID: `/subscriptions/5bd14da6-65ef-41c8-88ce-663170a1d6ff/resourcegroups/rg-wcus-p-compute-01/providers/microsoft.compute/disks/tigerwoodaz-datadisk-006-20260113-215044`
- **anteriadfwprod-datadisk** (microsoft.compute/disks)
  - Action: Change tier from 'P10 LRS Disk' to 'E10 LRS Disk'
  - ID: `/subscriptions/5bd14da6-65ef-41c8-88ce-663170a1d6ff/resourcegroups/anteriadfwprod/providers/microsoft.compute/disks/anteriadfwprod-datadisk`
- **seabeam-osdisk-00** (microsoft.compute/disks)
  - Action: Change tier from 'P15 LRS Disk' to 'E15 LRS Disk'
  - ID: `/subscriptions/5bd14da6-65ef-41c8-88ce-663170a1d6ff/resourcegroups/rg-wcus-p-compute-01/providers/microsoft.compute/disks/seabeam-osdisk-00`
- **apple-osdisk-00** (microsoft.compute/disks)
  - Action: Change tier from 'P15 LRS Disk' to 'E15 LRS Disk'
  - ID: `/subscriptions/5bd14da6-65ef-41c8-88ce-663170a1d6ff/resourcegroups/rg-wcus-p-compute-01/providers/microsoft.compute/disks/apple-osdisk-00`
- **banyan_osdisk_1_10b938c9de574a44968a66f239958d4a** (microsoft.compute/disks)
  - Action: Change tier from 'P15 LRS Disk' to 'E15 LRS Disk'
  - ID: `/subscriptions/5bd14da6-65ef-41c8-88ce-663170a1d6ff/resourcegroups/rg-wcus-p-compute-01/providers/microsoft.compute/disks/banyan_osdisk_1_10b938c9de574a44968a66f239958d4a`
- **mango_osdisk_1_3216a8c64fa742feb8d8f3596d41774a** (microsoft.compute/disks)
  - Action: Change tier from 'P10 LRS Disk' to 'E10 LRS Disk'
  - ID: `/subscriptions/5bd14da6-65ef-41c8-88ce-663170a1d6ff/resourcegroups/rg-wcus-p-compute-01/providers/microsoft.compute/disks/mango_osdisk_1_3216a8c64fa742feb8d8f3596d41774a`
- **maple-osdisk-00** (microsoft.compute/disks)
  - Action: Change tier from 'P15 LRS Disk' to 'E15 LRS Disk'
  - ID: `/subscriptions/5bd14da6-65ef-41c8-88ce-663170a1d6ff/resourcegroups/rg-wcus-p-compute-01/providers/microsoft.compute/disks/maple-osdisk-00`
- **datamart10-osdisk-00** (microsoft.compute/disks)
  - Action: Change tier from 'P30 LRS Disk' to 'E30 LRS Disk'
  - ID: `/subscriptions/5bd14da6-65ef-41c8-88ce-663170a1d6ff/resourcegroups/rg-wcus-p-compute-01/providers/microsoft.compute/disks/datamart10-osdisk-00`
- **vmweastnetdc01_osdisk_1_07adfe9d3df941c2aa3383f8d6769823** (microsoft.compute/disks)
  - Action: Change tier from 'P10 LRS Disk' to 'E10 LRS Disk'
  - ID: `/subscriptions/5bd14da6-65ef-41c8-88ce-663170a1d6ff/resourcegroups/anteriadryebrookprod/providers/microsoft.compute/disks/vmweastnetdc01_osdisk_1_07adfe9d3df941c2aa3383f8d6769823`
- **datamart2test-osdisk-00** (microsoft.compute/disks)
  - Action: Change tier from 'P10 LRS Disk' to 'E10 LRS Disk'
  - ID: `/subscriptions/5bd14da6-65ef-41c8-88ce-663170a1d6ff/resourcegroups/rg-wcus-d-compute-01/providers/microsoft.compute/disks/datamart2test-osdisk-00`
- **ninmada-osdisk-00** (microsoft.compute/disks)
  - Action: Change tier from 'P15 LRS Disk' to 'E15 LRS Disk'
  - ID: `/subscriptions/5bd14da6-65ef-41c8-88ce-663170a1d6ff/resourcegroups/rg-wcus-p-compute-01/providers/microsoft.compute/disks/ninmada-osdisk-00`
- **elderberry-osdisk-00** (microsoft.compute/disks)
  - Action: Change tier from 'P15 LRS Disk' to 'E15 LRS Disk'
  - ID: `/subscriptions/5bd14da6-65ef-41c8-88ce-663170a1d6ff/resourcegroups/rg-wcus-p-compute-01/providers/microsoft.compute/disks/elderberry-osdisk-00`
- **sassafras_osdisk_1_0c9b27fc98e14c578534283eac062616** (microsoft.compute/disks)
  - Action: Change tier from 'P10 LRS Disk' to 'E10 LRS Disk'
  - ID: `/subscriptions/5bd14da6-65ef-41c8-88ce-663170a1d6ff/resourcegroups/rg-wcus-p-compute-01/providers/microsoft.compute/disks/sassafras_osdisk_1_0c9b27fc98e14c578534283eac062616`
- **iasandbox_osdisk_1_2293ce9fb2444adf95a7021ba827134b** (microsoft.compute/disks)
  - Action: Change tier from 'P10 LRS Disk' to 'E10 LRS Disk'
  - ID: `/subscriptions/5bd14da6-65ef-41c8-88ce-663170a1d6ff/resourcegroups/rg-wcus-d-compute-01/providers/microsoft.compute/disks/iasandbox_osdisk_1_2293ce9fb2444adf95a7021ba827134b`
- **vmweastdmzdc01_osdisk_1_b9fa1843d5274d4da3a71ee0cabf4ab4** (microsoft.compute/disks)
  - Action: Change tier from 'P10 LRS Disk' to 'E10 LRS Disk'
  - ID: `/subscriptions/5bd14da6-65ef-41c8-88ce-663170a1d6ff/resourcegroups/anteriadryebrookprod/providers/microsoft.compute/disks/vmweastdmzdc01_osdisk_1_b9fa1843d5274d4da3a71ee0cabf4ab4`
- **testdapp-reports-osdisk-00** (microsoft.compute/disks)
  - Action: Change tier from 'P10 LRS Disk' to 'E10 LRS Disk'
  - ID: `/subscriptions/5bd14da6-65ef-41c8-88ce-663170a1d6ff/resourcegroups/rg-wcus-d-compute-01/providers/microsoft.compute/disks/testdapp-reports-osdisk-00`
- **lime_osdisk_1_aded19d37fed4ac391a11af433e807ca** (microsoft.compute/disks)
  - Action: Change tier from 'P10 LRS Disk' to 'S10 LRS Disk'
  - ID: `/subscriptions/5bd14da6-65ef-41c8-88ce-663170a1d6ff/resourcegroups/rg-wcus-p-compute-01/providers/microsoft.compute/disks/lime_osdisk_1_aded19d37fed4ac391a11af433e807ca`
- **walnut-osdisk-00** (microsoft.compute/disks)
  - Action: Change tier from 'P10 LRS Disk' to 'E10 LRS Disk'
  - ID: `/subscriptions/5bd14da6-65ef-41c8-88ce-663170a1d6ff/resourcegroups/rg-wcus-p-compute-01/providers/microsoft.compute/disks/walnut-osdisk-00`
- **dataiku-osdisk-00** (microsoft.compute/disks)
  - Action: Change tier from 'P10 LRS Disk' to 'E10 LRS Disk'
  - ID: `/subscriptions/5bd14da6-65ef-41c8-88ce-663170a1d6ff/resourcegroups/rg-wcus-p-compute-01/providers/microsoft.compute/disks/dataiku-osdisk-00`
- **datamart3-osdisk-00** (microsoft.compute/disks)
  - Action: Change tier from 'P20 LRS Disk' to 'E20 LRS Disk'
  - ID: `/subscriptions/5bd14da6-65ef-41c8-88ce-663170a1d6ff/resourcegroups/rg-wcus-p-compute-01/providers/microsoft.compute/disks/datamart3-osdisk-00`
- **sal_osdisk_1_582390e254484278b861b4f43f5b84de** (microsoft.compute/disks)
  - Action: Change tier from 'P15 LRS Disk' to 'E15 LRS Disk'
  - ID: `/subscriptions/5bd14da6-65ef-41c8-88ce-663170a1d6ff/resourcegroups/rg-wcus-p-compute-01/providers/microsoft.compute/disks/sal_osdisk_1_582390e254484278b861b4f43f5b84de`
- **linden_osdisk_1** (microsoft.compute/disks)
  - Action: Change tier from 'P20 LRS Disk' to 'E20 LRS Disk'
  - ID: `/subscriptions/5bd14da6-65ef-41c8-88ce-663170a1d6ff/resourcegroups/rg-wcus-p-storage-01/providers/microsoft.compute/disks/linden_osdisk_1`
- **vmwcushnetdc01_osdisk_1_576b5e89590641a299b0b3b5a564b83f** (microsoft.compute/disks)
  - Action: Change tier from 'P10 LRS Disk' to 'S10 LRS Disk'
  - ID: `/subscriptions/5bd14da6-65ef-41c8-88ce-663170a1d6ff/resourcegroups/rg-wcus-h-compute-01/providers/microsoft.compute/disks/vmwcushnetdc01_osdisk_1_576b5e89590641a299b0b3b5a564b83f`
- **vmwcushnetdc02_osdisk_1_618c0a9993974639aad12f7f5678f0f4** (microsoft.compute/disks)
  - Action: Change tier from 'P10 LRS Disk' to 'S10 LRS Disk'
  - ID: `/subscriptions/5bd14da6-65ef-41c8-88ce-663170a1d6ff/resourcegroups/rg-wcus-h-compute-01/providers/microsoft.compute/disks/vmwcushnetdc02_osdisk_1_618c0a9993974639aad12f7f5678f0f4`
- **vmwcushapps01_osdisk_1_fb9e48ec9b494ca9bde97f9927df9d23** (microsoft.compute/disks)
  - Action: Change tier from 'P10 LRS Disk' to 'E10 LRS Disk'
  - ID: `/subscriptions/5bd14da6-65ef-41c8-88ce-663170a1d6ff/resourcegroups/rg-wcus-p-compute-01/providers/microsoft.compute/disks/vmwcushapps01_osdisk_1_fb9e48ec9b494ca9bde97f9927df9d23`
- **datamart2az_osdisk_1_e01ee87cfb3c4e0aabbd2edead893ab1** (microsoft.compute/disks)
  - Action: Change tier from 'P10 LRS Disk' to 'E10 LRS Disk'
  - ID: `/subscriptions/5bd14da6-65ef-41c8-88ce-663170a1d6ff/resourcegroups/rg-wcus-p-compute-01/providers/microsoft.compute/disks/datamart2az_osdisk_1_e01ee87cfb3c4e0aabbd2edead893ab1`
- **mrtdatamart2az_osdisk_1_c3712f8b06714fc584b49b07bea60a2f** (microsoft.compute/disks)
  - Action: Change tier from 'P10 LRS Disk' to 'E10 LRS Disk'
  - ID: `/subscriptions/5bd14da6-65ef-41c8-88ce-663170a1d6ff/resourcegroups/rg-wcus-p-compute-01/providers/microsoft.compute/disks/mrtdatamart2az_osdisk_1_c3712f8b06714fc584b49b07bea60a2f`
- **dd-osdisk-00** (microsoft.compute/disks)
  - Action: Change tier from 'P10 LRS Disk' to 'E10 LRS Disk'
  - ID: `/subscriptions/5bd14da6-65ef-41c8-88ce-663170a1d6ff/resourcegroups/rg-wcus-a-compute-01/providers/microsoft.compute/disks/dd-osdisk-00`
- **hd-dapp-reports-osdisk-00** (microsoft.compute/disks)
  - Action: Change tier from 'P10 LRS Disk' to 'E10 LRS Disk'
  - ID: `/subscriptions/5bd14da6-65ef-41c8-88ce-663170a1d6ff/resourcegroups/rg-wcus-a-compute-01/providers/microsoft.compute/disks/hd-dapp-reports-osdisk-00`
- **wolffish-osdisk-00** (microsoft.compute/disks)
  - Action: Change tier from 'P10 LRS Disk' to 'E10 LRS Disk'
  - ID: `/subscriptions/5bd14da6-65ef-41c8-88ce-663170a1d6ff/resourcegroups/rg-wcus-a-compute-01/providers/microsoft.compute/disks/wolffish-osdisk-00`
- **thomagataaz_osdisk_1_341d1390c0e1467a8e0d145a8f1fa487** (microsoft.compute/disks)
  - Action: Change tier from 'P10 LRS Disk' to 'S10 LRS Disk'
  - ID: `/subscriptions/5bd14da6-65ef-41c8-88ce-663170a1d6ff/resourcegroups/rg-wcus-p-compute-01/providers/microsoft.compute/disks/thomagataaz_osdisk_1_341d1390c0e1467a8e0d145a8f1fa487`
- **meritanalyticsaz_osdisk_1_f43b7f5ae4c34e7aa19ea5fd66e3bfda** (microsoft.compute/disks)
  - Action: Change tier from 'P10 LRS Disk' to 'S10 LRS Disk'
  - ID: `/subscriptions/5bd14da6-65ef-41c8-88ce-663170a1d6ff/resourcegroups/rg-wcus-p-compute-01/providers/microsoft.compute/disks/meritanalyticsaz_osdisk_1_f43b7f5ae4c34e7aa19ea5fd66e3bfda`
- **spot-osdisk-00** (microsoft.compute/disks)
  - Action: Change tier from 'P10 LRS Disk' to 'E10 LRS Disk'
  - ID: `/subscriptions/5bd14da6-65ef-41c8-88ce-663170a1d6ff/resourcegroups/rg-wcus-p-compute-01/providers/microsoft.compute/disks/spot-osdisk-00`
- **dev-elderberry_osdisk_1_3108fd3dfb53476ca8180050f38ff53c** (microsoft.compute/disks)
  - Action: Change tier from 'P10 LRS Disk' to 'S10 LRS Disk'
  - ID: `/subscriptions/5bd14da6-65ef-41c8-88ce-663170a1d6ff/resourcegroups/wcus-dev-pmd-vm01/providers/microsoft.compute/disks/dev-elderberry_osdisk_1_3108fd3dfb53476ca8180050f38ff53c`
- **vmweastmddc02_disk1_cec6b65af8f1400d84f91491e673b9e1** (microsoft.compute/disks)
  - Action: Change tier from 'P10 LRS Disk' to 'E10 LRS Disk'
  - ID: `/subscriptions/5bd14da6-65ef-41c8-88ce-663170a1d6ff/resourcegroups/anteriadryebrookprod/providers/microsoft.compute/disks/vmweastmddc02_disk1_cec6b65af8f1400d84f91491e673b9e1`
- **vmweastmddc01_disk1_036bd8b2069c4c72b83c75e37214f8e1** (microsoft.compute/disks)
  - Action: Change tier from 'P10 LRS Disk' to 'S10 LRS Disk'
  - ID: `/subscriptions/5bd14da6-65ef-41c8-88ce-663170a1d6ff/resourcegroups/anteriadryebrookprod/providers/microsoft.compute/disks/vmweastmddc01_disk1_036bd8b2069c4c72b83c75e37214f8e1`
- **mdw1014res-osdisk-20251227-070633** (microsoft.compute/disks)
  - Action: Change tier from 'P15 LRS Disk' to 'E15 LRS Disk'
  - ID: `/subscriptions/5bd14da6-65ef-41c8-88ce-663170a1d6ff/resourcegroups/anteriadryebrookprod/providers/microsoft.compute/disks/mdw1014res-osdisk-20251227-070633`
- **ssgcobrares-osdisk-20251227-064640** (microsoft.compute/disks)
  - Action: Change tier from 'P20 LRS Disk' to 'E20 LRS Disk'
  - ID: `/subscriptions/5bd14da6-65ef-41c8-88ce-663170a1d6ff/resourcegroups/anteriadryebrookprod/providers/microsoft.compute/disks/ssgcobrares-osdisk-20251227-064640`
- **mdsql02-osdisk-20251227-182427** (microsoft.compute/disks)
  - Action: Change tier from 'P15 LRS Disk' to 'E15 LRS Disk'
  - ID: `/subscriptions/5bd14da6-65ef-41c8-88ce-663170a1d6ff/resourcegroups/anteriadryebrookprod/providers/microsoft.compute/disks/mdsql02-osdisk-20251227-182427`
- **firstlogic-osdisk-00** (microsoft.compute/disks)
  - Action: Change tier from 'P15 LRS Disk' to 'E15 LRS Disk'
  - ID: `/subscriptions/5bd14da6-65ef-41c8-88ce-663170a1d6ff/resourcegroups/rg-wcus-p-compute-01/providers/microsoft.compute/disks/firstlogic-osdisk-00`
- **empress-whsp-osdisk-00** (microsoft.compute/disks)
  - Action: Change tier from 'P10 LRS Disk' to 'E10 LRS Disk'
  - ID: `/subscriptions/5bd14da6-65ef-41c8-88ce-663170a1d6ff/resourcegroups/rg-wcus-p-compute-01/providers/microsoft.compute/disks/empress-whsp-osdisk-00`
- **mrtdatamart1az_osdisk_1_3c63d9392b814dff8d30864357626cf1** (microsoft.compute/disks)
  - Action: Change tier from 'P10 LRS Disk' to 'E10 LRS Disk'
  - ID: `/subscriptions/5bd14da6-65ef-41c8-88ce-663170a1d6ff/resourcegroups/rg-wcus-p-compute-01/providers/microsoft.compute/disks/mrtdatamart1az_osdisk_1_3c63d9392b814dff8d30864357626cf1`
- **vmwcusvdi-whs_osdisk_1_6b37b7dd258341f994e95ed328cb5b05** (microsoft.compute/disks)
  - Action: Change tier from 'P10 LRS Disk' to 'E10 LRS Disk'
  - ID: `/subscriptions/5bd14da6-65ef-41c8-88ce-663170a1d6ff/resourcegroups/rg-wcus-p-compute-01/providers/microsoft.compute/disks/vmwcusvdi-whs_osdisk_1_6b37b7dd258341f994e95ed328cb5b05`
- **wcusdevitvm02_osdisk_1_aca2e4d12d1b438a8be584c7776103fa** (microsoft.compute/disks)
  - Action: Change tier from 'P10 LRS Disk' to 'E10 LRS Disk'
  - ID: `/subscriptions/5bd14da6-65ef-41c8-88ce-663170a1d6ff/resourcegroups/rg-wcus-d-compute-01/providers/microsoft.compute/disks/wcusdevitvm02_osdisk_1_aca2e4d12d1b438a8be584c7776103fa`
- **alps_p30stripe2** (microsoft.compute/disks)
  - Action: Change tier from 'P30 LRS Disk' to 'E30 LRS Disk'
  - ID: `/subscriptions/348c3a20-66f6-421a-b21c-97bb55449b11/resourcegroups/meriteuprod/providers/microsoft.compute/disks/alps_p30stripe2`
- **alps_p30stripe6** (microsoft.compute/disks)
  - Action: Change tier from 'P30 LRS Disk' to 'E30 LRS Disk'
  - ID: `/subscriptions/348c3a20-66f6-421a-b21c-97bb55449b11/resourcegroups/meriteuprod/providers/microsoft.compute/disks/alps_p30stripe6`
- **alps_p30stripe7** (microsoft.compute/disks)
  - Action: Change tier from 'P30 LRS Disk' to 'E30 LRS Disk'
  - ID: `/subscriptions/348c3a20-66f6-421a-b21c-97bb55449b11/resourcegroups/meriteuprod/providers/microsoft.compute/disks/alps_p30stripe7`
- **alps_p30stripe3** (microsoft.compute/disks)
  - Action: Change tier from 'P30 LRS Disk' to 'E30 LRS Disk'
  - ID: `/subscriptions/348c3a20-66f6-421a-b21c-97bb55449b11/resourcegroups/meriteuprod/providers/microsoft.compute/disks/alps_p30stripe3`
- **alps_sql_log** (microsoft.compute/disks)
  - Action: Change tier from 'P30 LRS Disk' to 'E30 LRS Disk'
  - ID: `/subscriptions/348c3a20-66f6-421a-b21c-97bb55449b11/resourcegroups/meriteuprod/providers/microsoft.compute/disks/alps_sql_log`
- **alps_p30stripe4** (microsoft.compute/disks)
  - Action: Change tier from 'P30 LRS Disk' to 'E30 LRS Disk'
  - ID: `/subscriptions/348c3a20-66f6-421a-b21c-97bb55449b11/resourcegroups/meriteuprod/providers/microsoft.compute/disks/alps_p30stripe4`
- **alps_p30stripe5** (microsoft.compute/disks)
  - Action: Change tier from 'P30 LRS Disk' to 'E30 LRS Disk'
  - ID: `/subscriptions/348c3a20-66f6-421a-b21c-97bb55449b11/resourcegroups/meriteuprod/providers/microsoft.compute/disks/alps_p30stripe5`
- **alps_p30stripe1** (microsoft.compute/disks)
  - Action: Change tier from 'P30 LRS Disk' to 'E30 LRS Disk'
  - ID: `/subscriptions/348c3a20-66f6-421a-b21c-97bb55449b11/resourcegroups/meriteuprod/providers/microsoft.compute/disks/alps_p30stripe1`
- **alps_database1** (microsoft.compute/disks)
  - Action: Change tier from 'P50 LRS Disk' to 'E50 LRS Disk'
  - ID: `/subscriptions/348c3a20-66f6-421a-b21c-97bb55449b11/resourcegroups/meriteuprod/providers/microsoft.compute/disks/alps_database1`
- **scandinavianres-osdisk-20251226-222154** (microsoft.compute/disks)
  - Action: Change tier from 'E10 LRS Disk' to 'S10 LRS Disk'
  - ID: `/subscriptions/348c3a20-66f6-421a-b21c-97bb55449b11/resourcegroups/meriteuprod/providers/microsoft.compute/disks/scandinavianres-osdisk-20251226-222154`
- **alps-osdisk-20251227-014001** (microsoft.compute/disks)
  - Action: Change tier from 'E20 LRS Disk' to 'S20 LRS Disk'
  - ID: `/subscriptions/348c3a20-66f6-421a-b21c-97bb55449b11/resourcegroups/meriteuprod/providers/microsoft.compute/disks/alps-osdisk-20251227-014001`
- **alps-datadisk-000-20251227-014001** (microsoft.compute/disks)
  - Action: Change tier from 'P50 LRS Disk' to 'E50 LRS Disk'
  - ID: `/subscriptions/348c3a20-66f6-421a-b21c-97bb55449b11/resourcegroups/meriteuprod/providers/microsoft.compute/disks/alps-datadisk-000-20251227-014001`
- **dolomitesres-osdisk-20251227-003319** (microsoft.compute/disks)
  - Action: Change tier from 'E10 LRS Disk' to 'S10 LRS Disk'
  - ID: `/subscriptions/348c3a20-66f6-421a-b21c-97bb55449b11/resourcegroups/meriteuprod/providers/microsoft.compute/disks/dolomitesres-osdisk-20251227-003319`
- **pyreneesres-osdisk-20251227-002723** (microsoft.compute/disks)
  - Action: Change tier from 'E10 LRS Disk' to 'S10 LRS Disk'
  - ID: `/subscriptions/348c3a20-66f6-421a-b21c-97bb55449b11/resourcegroups/meriteuprod/providers/microsoft.compute/disks/pyreneesres-osdisk-20251227-002723`
- **carpathianres-osdisk-20251227-182131** (microsoft.compute/disks)
  - Action: Change tier from 'E10 LRS Disk' to 'S10 LRS Disk'
  - ID: `/subscriptions/348c3a20-66f6-421a-b21c-97bb55449b11/resourcegroups/meriteuprod/providers/microsoft.compute/disks/carpathianres-osdisk-20251227-182131`
- **vmweumddc01_osdisk_1_0684465199bc4d6084cc4aa1107a4709** (microsoft.compute/disks)
  - Action: Change tier from 'P10 LRS Disk' to 'S10 LRS Disk'
  - ID: `/subscriptions/348c3a20-66f6-421a-b21c-97bb55449b11/resourcegroups/meriteuprod/providers/microsoft.compute/disks/vmweumddc01_osdisk_1_0684465199bc4d6084cc4aa1107a4709`
- **vmweudmzdc01_osdisk_1_c1a369be48c9487b9d06e339b9be8abb** (microsoft.compute/disks)
  - Action: Change tier from 'P10 LRS Disk' to 'E10 LRS Disk'
  - ID: `/subscriptions/348c3a20-66f6-421a-b21c-97bb55449b11/resourcegroups/meriteuprod/providers/microsoft.compute/disks/vmweudmzdc01_osdisk_1_c1a369be48c9487b9d06e339b9be8abb`
- **vmweunetdc01_osdisk_1_e80e2746f2964ae5a5560a37454fff76** (microsoft.compute/disks)
  - Action: Change tier from 'P10 LRS Disk' to 'S10 LRS Disk'
  - ID: `/subscriptions/348c3a20-66f6-421a-b21c-97bb55449b11/resourcegroups/meriteuprod/providers/microsoft.compute/disks/vmweunetdc01_osdisk_1_e80e2746f2964ae5a5560a37454fff76`
- **vmweudeudc001_osdisk_1_e1ec9ec0c1bf4730bb410a6ff9c4b1aa** (microsoft.compute/disks)
  - Action: Change tier from 'P10 LRS Disk' to 'E10 LRS Disk'
  - ID: `/subscriptions/348c3a20-66f6-421a-b21c-97bb55449b11/resourcegroups/meriteuprod/providers/microsoft.compute/disks/vmweudeudc001_osdisk_1_e1ec9ec0c1bf4730bb410a6ff9c4b1aa`
- **vmweudeudc002_osdisk_1_94a54ed2663747a48258adb76df6203b** (microsoft.compute/disks)
  - Action: Change tier from 'P10 LRS Disk' to 'E10 LRS Disk'
  - ID: `/subscriptions/348c3a20-66f6-421a-b21c-97bb55449b11/resourcegroups/meriteuprod/providers/microsoft.compute/disks/vmweudeudc002_osdisk_1_94a54ed2663747a48258adb76df6203b`
- **vmweudeudc02res-osdisk-20251226-202640** (microsoft.compute/disks)
  - Action: Change tier from 'P10 LRS Disk' to 'S10 LRS Disk'
  - ID: `/subscriptions/348c3a20-66f6-421a-b21c-97bb55449b11/resourcegroups/meriteuprod/providers/microsoft.compute/disks/vmweudeudc02res-osdisk-20251226-202640`
- **vmweudeudc01res-osdisk-20251226-205157** (microsoft.compute/disks)
  - Action: Change tier from 'P10 LRS Disk' to 'S10 LRS Disk'
  - ID: `/subscriptions/348c3a20-66f6-421a-b21c-97bb55449b11/resourcegroups/meriteuprod/providers/microsoft.compute/disks/vmweudeudc01res-osdisk-20251226-205157`

## Remediation Steps
*No remediation steps provided*

---
*This document was auto-generated from vBox task data.*
