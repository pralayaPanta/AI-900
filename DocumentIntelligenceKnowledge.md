- [Fundamental of Azure AI Document Intelligence](#fundamental-of-azure-ai-document-intelligence)
    - [Azure AI Document Intelligence Models](#azure-ai-document-intelligence-models)
    - [Receipt analysis on Azure](#receipt-analysis-on-azure)
- [Fundamentals of Knowledge Mining and Azure AI Search](#fundamentals-of-knowledge-mining-and-azure-ai-search)
    - [What is Azure AI Search?](#what-is-azure-ai-search)
    - [Elements of Azure AI Search](#elements-of-azure-ai-search)
    - [Indexes](#indexes)
    - [Indexer](#indexer)
    - [Knowledge Store](#knowledge-store)
    - [Create an index in Azure Portal](#create-an-index-in-azure-portal)
    - [Review](#review)


# Fundamental of Azure AI Document Intelligence

- Document intelligence relies on machine learning models that are trained to recognise data in text.
- _Document analysis_ is the ability to extract text, layout, and key value pairs
- To use Azure AI Document Intelligence, create either a Document Intelligence or Azure AI services resource in your Azure subscription.
  
### Azure AI Document Intelligence Models

- Prebuilt Model - have been built to process common doc type and extracts specific field that are important.
- Custom Model - can be trained to identify specific field that are not included in pretrained model
- Document Analysis - general document analysis that returns structured data representations, including regions of intereset and relationships

### Receipt analysis on Azure
- Prebuilt model
- processes receipt by
    - matching field names to values
    - identifying tables of data
    - identifying specific fields, such as dates, telephone numbers, addresses, and other
- can recognise data on serveral type, thermal receipts, hotel receipts, gas receipts, parking receipts etc



# Fundamentals of Knowledge Mining and Azure AI Search

### What is Azure AI Search?
- provides the infrastructure and tools to create search solutions that extract data from various structured, semi-structured, and non-structured documents.
- Features
      - Data from any source - source JSON format
      - Full text search and analysis
      - AI powered search
      - Multi-lingual offers - 56 lang
      - Geo-enabled
      - COnfigurable user experience

### Elements of Azure AI Search

1. Data sources
      -    contains data artifacts to be searched
      -    could be files and folders in azure storage, text in a database
      -    Azure AI Search supports JSON data format
      -    If JSON document, the search engine can index
2. Indexer
      -    automates data ingestion and JSON serialisation of source data
      -    passess to the search esngine for indexing
      -    data enrichment 

3. Skillset for encrichment pipeline
      -   skillset defines the operations that extract and enrich data to make it searchable.
      -    examples
           - builtin skills
               - natural language processing skills
                   - key phrase extraction
                   - tex translations skill
               - image processing kills
                 - image analysis skills
                 - optical character recognition skill
           - custom skills
  
### Indexes
   - index as a table and each row in the table represents a document
     - each document is a single unit of searchable data in the index
   - collection of JSON documents
   - The index includes a definition of the structure of the data called schema
   - Index attributes are behaviors of the indexes
   - Example
        ```
        {
            "name": " index" ,
            "fields " :[
                {
                    "name": "content" , "type": "Edm.String", "analyzer": "standard . lucene", "fields " :[]
                },
                {
                    "name" : "keyphrases", "type": "Collection(Edm.String), "analyzer": "standard. lucene", "fields " :[]
                },
                {
                    "name": "imageTags", "type": "Collection(Edm.String),"analyzer": "standard. lucene" , "fields " :[]
                },
            ]
        }

### Indexer
   - JSON can be generated with application or using Azure Indexer
     - it exports incoming documents into JSON
   - Create and load using two methods
         1.    Push method - JSON document is pushed into a search index via either the REST API or .NET SDK
         2.    Pull method - From popular data source from Azure
   
   - Pull method
         - Azure AI Search's indexer is a crawler that extracts searchable text and metdadata from ane external Azure data source and populates search index
         - An indexer maps source fields to their matching fields in the index


### Knowledge Store
   - persistent storage of encriched content
   - stores the data generated from AI encrichment in a container
   - Skillsets move a document through sequence of enrichment which can be a search index or projections in a knowledge store.
   - Types of projection
       - table projection
       - object projection
       - file projection

### Create an index in Azure Portal
   - Supported data source
       - Cosmos DB
       - Azure SQL
       - Azure Storage
     - Query data
       - A query is a list or words and query operators of what you would like to see returned in a result set.
       - types
           - simple
           - full lucene

### Review

   - _**Data Source**_: Persists connection information to source data, including credentials. A data source object is used exclusively with indexers.
   - _**Index**_: Physical data structure used for full text search and other queries.
   - _**Indexer**_: A configuration object specifying a data source, target index, an optional AI skillset, optional schedule, and optional configuration settings for error handling and base-64 encoding.
   - _**Skillset**_: A complete set of instructions for manipulating, transforming, and shaping content, including analyzing and extracting information from image files. Except for very simple and limited structures, it includes a reference to an Azure AI services resource that provides enrichment.
   - _**Knowledge store**_: Stores output from an AI enrichment pipeline in tables and blobs in Azure Storage for independent analysis or downstream processing.