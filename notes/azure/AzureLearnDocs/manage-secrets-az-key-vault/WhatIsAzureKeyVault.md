# Microsoft Azure Learn Notes: Manage Secrets in your server apps with Key Vault [What is Azure Key Vault?](https://docs.microsoft.com/en-us/learn/modules/manage-secrets-with-azure-key-vault/2-what-is-key-vault)

## Last Edited `02/21/2021`

---  

## Notes' Author List

1. [Trevor Henderson](https://github.com/trevor-henderson)

---  

## Notable Definitions (Legend)

| Key | Description | Link |  
|-------------|-------------|-------------|  
| `Vault` | Azure Resources used to group secrets together | N/A |  

---  

## Benefits of Key Vault  
- Separation of secrets from code configuration -> Reduce accidental leaks.  
- Restrict Secret Access  
- Centralize Secret Storage  
- Observability(Logging and Monitoring) of Secret Access  

---  

## Overview  
- Secrets are stored in individual `vaults`  
- Secret access/vault management is done via REST API  
- Every `Vault` has a unique URL where it's respective API is hosted  

_Note:_ Key Vault is designed to store configuration. Never use it to store runtime application data.  

---  

## What is a Secret in Key Vault?  
- Key-Value pair of strings  
- Rules for Secrets:
    - 1 - 127 characters long  
    - Alphanumeric characters and dashes are considered valid  
    - UTF-8 strings up to 25 KB in size are considered valid  
    - Additional Support beyond strings for `Keys and Certificates`(_Not covered in this module_)  

---  

## Vault Authentication and Permissions  
- Uses Azure Active Directory to authenticate users and apps  
- `Vault` access policies are based on _actions_ that users or applications will have assinged permissions for.  
- All _actions_ require authentication & authorization. No anonymous authentication
- `Vault` _actions_ Examples:  
      - `Get`: read secret values from the `Vault`  
      - `Set`: create or update secret values  
      - `List`: List all names of secretes  

---  

**Module 2: What Is Azure Key Vault?**  
