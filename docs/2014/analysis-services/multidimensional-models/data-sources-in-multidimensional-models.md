---
title: "Data Sources in Multidimensional Models | Microsoft Docs"
ms.custom: ""
ms.date: "06/13/2017"
ms.prod: "sql-server-2014"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "analysis-services"
ms.tgt_pltfrm: ""
ms.topic: conceptual
helpviewer_keywords: 
  - "metadata [Analysis Services]"
  - "Analysis Services objects, data sources"
  - "storing data [Analysis Services], data sources"
  - "data sources [Analysis Services], about data sources"
  - "security [Analysis Services], data sources"
  - "data sources [Analysis Services]"
  - "storage [Analysis Services], data sources"
ms.assetid: a16469d9-9d53-4e35-9982-fc06327a9d33
caps.latest.revision: 44
author: "Minewiskan"
ms.author: "owend"
manager: "mblythe"
---
# Data Sources in Multidimensional Models
  All data that you import or load into a multidimensional model originates from an external data source. Typically, source data is from a data warehouse designed for reporting purposes, but it could come from any relational database that is accessed directly or indirectly through an intermediary, such as an [!INCLUDE[ssIS](../../includes/ssis-md.md)] package.  
  
 A **data source** object in [!INCLUDE[ssASnoversion](../../includes/ssasnoversion-md.md)] specifies a direct connection to an external data source. In addition to physical location, a data source object specifies the connection string, data provider, credentials, and other properties that control connection behavior.  
  
 Information provided by the data source object is used during the following operations:  
  
-   Get schema information and other metadata used to generate data source views into a model.  
  
-   Query or load data into a model during processing.  
  
-   Run queries against multidimensional or data mining models that use ROLAP storage mode.  
  
-   Read or write to remote partitions.  
  
-   Connect to linked objects, as well as synchronize from target to source.  
  
-   Perform write back operations that update fact table data stored in a relational database.  
  
 When building a multidimensional model from the bottom up, you start by creating the data source object, and then use it to generate the next object, a **data source view**. A data source view is the data abstraction layer in the model. It is typically created after the data source object, using the schema of the source database as the basis. However, you can choose other ways to build a model, including starting with cubes and dimensions, and generating the schema that best supports your design.  
  
 Regardless of how you build it, each model requires at least one data source object that specifies a connection to source data. You can create multiple data source objects in a single model to use data from different sources or vary connection properties for specific objects.  
  
 Data source objects can be managed independently of other objects in your model. After you create a data source, you can change its properties later, and then preprocess the model to ensure the data is retrieved correctly.  
  
## Related Topics and Tasks  
  
|Topic|Description|  
|-----------|-----------------|  
|[Data Sources Supported &#40;SSAS Multidimensional&#41;](supported-data-sources-ssas-multidimensional.md)|Describes the types of data sources that can be used in a multidimensional model.|  
|[Create a Data Source &#40;SSAS Multidimensional&#41;](create-a-data-source-ssas-multidimensional.md)|Explains how to add a data source object to a multidimensional model.|  
|[Delete a Data Source in Solution Explorer &#40;SSAS Multidimensional&#41;](delete-a-data-source-in-solution-explorer-ssas-multidimensional.md)|Use this procedure to delete a data source object from a multidimensional model.|  
|[Set Data Source Properties &#40;SSAS Multidimensional&#41;](set-data-source-properties-ssas-multidimensional.md)|Describes each property and explains how to set each one.|  
|[Set Impersonation Options &#40;SSAS - Multidimensional&#41;](set-impersonation-options-ssas-multidimensional.md)|Explains how to configure options in the Impersonation Information dialog box.|  
  
## See Also  
 [Database Objects &#40;Analysis Services - Multidimensional Data&#41;](olap-logical/database-objects-analysis-services-multidimensional-data.md)   
 [Logical Architecture &#40;Analysis Services - Multidimensional Data&#41;](olap-logical/understanding-microsoft-olap-logical-architecture.md)   
 [Data Source Views in Multidimensional Models](data-source-views-in-multidimensional-models.md)   
 [Data Sources and Bindings &#40;SSAS Multidimensional&#41;](data-sources-and-bindings-ssas-multidimensional.md)  
  
  