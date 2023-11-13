# On-premise Data Migration Project into Azure

* The main objective of the project is to move all the tables from the on-premise SQL server to Azure.
*	Created Azure Data factory pipeline to migrate the data from on-premise to Azure by using  Azure self-hosted integration runtime.
*	Used Lookup, For each and copy activity within ADF to iteratively move all the tables from on-premise to Azure by using the dynamic content option.
* Configured appropriate source, sink, and file format options while moving the data into Azure Data Lake Gen 2.
*	Then used Azure Databricks to transform the data by categorizing them into bronze, silver, and gold layers by mounting the Azure Data Lake gen2 by creating the app registration, and then adding the role assignment.
*	Integrated this Azure data bricks notebook in the ADF to automatically do the transformation once they are available at the source.
*	To analyze the cleaned data we used Azure Synapse Analytics. We mounted the gold container which has the cleaned data.
*	Created another pipeline in the Synapse which uses the get metadata, for each and stored procedure activity to dynamically create the view for all the files present in the ADLS.
*	Once we created the view we analyzed the data to get insights from the data using a serverless SQL pool.
*	To build the interactive visualization we use PowerBI. We connected the PowerBI with the Synapse analytics using the Synapse SQL server endpoint and then visualized the data in PowerBI.
*	Used Azure key vault and active directory  in managing and safeguarding cryptographic keys and user access.


  ![image](https://github.com/akshay-venur/Data-Migration-Using-Azure/assets/43615481/96872148-9c1b-4c50-8d58-8970e9a7ada7)

