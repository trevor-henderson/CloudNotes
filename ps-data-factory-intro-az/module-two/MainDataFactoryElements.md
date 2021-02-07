# Main Data Factory Elements  

## Last Edited `02/07/2021`

---  

## Notes' Author List

1. [Trevor Henderson](https://github.com/trevor-henderson)

---  

## Notable Definitions (Legend)

| Key | Description | Link |  
|-------------|-------------|-------------|  

---  

## Main Elements  
- `Activities`  
  - Represents each step where some action may be taken with the Data
- `Pipelines`
    - Logical grouping of all activities to perform a unit of work.
- `Integration Runtines`  
    - The Compute infrastructure for ADF
- `Triggers`  
  - Tells ADF when to run certain activities  
- `Datasets`
  - The data you are working with  
- `Linked Services`  
  - Like a trait. Essentially connection strings  

---  

## Element Relationships
- An `Activity` will consume/produce data from/to a given `Data Set`  
- A `Pipeline` will create a logical grouping for `Activities`
- A `Linked Service` might be what the `Data Set` represents or what an `Activity` might run on  

---  

## Microsoft ETL Terminology  

### Cloud to On-Prem comparison  

| Azure Data Factory | Integration Services |  
|--------------------|----------------------|
| `Pipeline` | `Package`|  
| `Activities` | `Task` |  
| `Linked Services` | `Connection Managers` |  
| `Datasets` | `SSIS Sources and Destinations` |  
| `Sources/Sink` | `Source/Destination` |  
| `Json files` | `DTSX (XML)` |  

---  

## Activities and Pipelines  
- Advantage of the `Pipeline` is that it allows you to view your `Activities` as a set  
    - Development & scheduling happen at the `Pipeline` level  
- `Activities` are where the work happens with three types of `Activities`  
    1. `Copy Activity`  
        - 80 different connectors  
        - Pull data from a source(i.e. SQL Server)  
    1. `Transformation Activity`  
        - Set options for external services  
        - Transforms data across the pipeline  
    1. `Data Control Activity`  
        - Control flow of pipeline  

---  

**Module 2 Lecture 3**