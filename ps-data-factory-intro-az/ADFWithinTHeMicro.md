# Data Factories within Microsoft's environment  

## Last Edited `02/07/2021`

---  

## Notes' Author List

1. [Trevor Henderson](https://github.com/trevor-henderson)

---  

## Notable Definitions (Legend)

| Key | Description | Link |  
|-------------|-------------|-------------|  

---  

## Data Factory on Azure's Ecosystem  

- What Problem are you solving for?  
  - Migration?  
    - If simple database migration from on-prem to cloud
    utilize existing services  
    - ADF Excels on periodic data loads/transformations  
  - Streaming?
    - Best to use separate services dedicated to this
  - Transformations?
    - Bingo  
---  

## SSIS vs. ADF  
- SSIS  
  - More code-free transformations  
  - On-Prem connectors like Excel  
- ADF  
  - Much Higher Scalability  
  - Cloud and SaaS Connectors  
  - Can be event-driven  
  - Runs SSIS packages  

---  

## Data Factory Considerations  
- v1  
  - Worked mostly through JSON files
- v2  
  - Has UI to interact
- Build options  
  - Powershell, .NET, Python, REST, ARM  
- Highly integrated  
  - DevOps, Key Vault, Monitor, Automation, etc.
- No data storage persistence  
  - You need to persist data at an end state  
