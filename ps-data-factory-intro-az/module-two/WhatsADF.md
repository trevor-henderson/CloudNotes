# Understanding Azure Data Factory  

## Last Edited `02/07/2021`

---  

## Notes' Author List

1. [Trevor Henderson](https://github.com/trevor-henderson)

---  

## Notable Definitions (Legend)  

| Term | expanded name | Meaning |  
|------|---------------|---------|
| `ADF` |Azure Data Factory| Data Integration Service that allows you to orchestrate and automate the movement and transformation of data. |
| `MS` | Microsoft | N/A |  
| `ETL` | Extract Translate Load | Pattern for handling data flowing through a pipeline |  
| `ELT` | Extract Load Translate | Pattern for handling data flowing through a pipeline |  

---  

## So ... uh ... what is Azure Data Factory?  

- Before answering that Why us ADF?
  - due to Variety, Velocity, and volume of data Data insights 
    are a necessity for keeping a competitive edge  
  - ADF is MS main data engineering tool
    
- ADF
  - PaaS Solution  
  - Data Integration Service  
  - Over 88 connectors for orchestration & automation  
  - Data Transformation  
  - Out of the box _codeless_ functionality for joining or otherwise aggregating data through the pipeline

- ETL/ELT: How does data flow through ADF / what side effects are applied to the data
  - ELT => Agility  
      - Developers can change queries on the fly  
      - Lends well for PoC or continuous optimization  
  - ETL => Reliability  
    - High degree that data will be well-structured and compliant
  - In ADF
    - Can do either ELT/ETL
    - Third party services to aid in translation/aggregation

---  

**Module 2 Lecture 1**