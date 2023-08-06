
# **3B_ExportSourceDataToParquet:** Export source data to Parquet-files

As an alternative to exporting data using Polybase, you can use a PowerShell-script which extracts data from source databases to Parquet-files. The script is available under [/Migration/SQLServer/2B_ExportSourceDataToParquet](../../SQLServer/2B_ExportSourceDataToParquet) folder (it is applicable to APS/PDW too). It allows to offload data to Parquet-files on a local storage, network storage, or Azure Data Box appliance without configuring Polybase.

Generated Parquet-files should be transferred to Azure storage either over a wire or by using Azure Data Box service.

> Note that SELECT-queries generated by the script consume APS/PDW concurrency slots and data is offloaded via control node. Therefore, overall appliance performance impact should be carefully considered.