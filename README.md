# Versioning

## Overview of the git commit coonvention

- Format of the commit message; `(<scope>)` is optional

  ```
  <type>(<scope>)[<branch id>]: <subject>
  <BLANK LINE>
  <body>
  <BLANK LINE>
  <footer>
  ```
  
  - Examples:
  
    ```
    doc([common]CHANGELOG.md)[13]: Update Unreleased section
    ```
    ```
    feat(frontend)[13]: add fnCleanHTML

    - description
    - description
    ```
    
- Allowed <type>; configurable

  - **feat** (feature)
  - **fix** (bug fix)
  - **docs** (documentation)
  - **style** (formatting, missing semi colons, …)
  - **refactor**
  - **test** (when adding missing tests)
  - **chore** (maintain)
  
- Allowed <scope>; configurable; `(<scope>)` is optional

  - **admin-area**
  - **wallet-area**
  - **merchant-area**
  - **public-area**
  - **backend**
  - **frontend**
  - **common**
  - `<[<parent scope>]<child scope>>`
  
    `<parent scope>` it is any of `<scope>`
    
    `<parent scope>` is required when you use `<child scope>`
    
    - Allowed `<child scope>`
    
      - filename/folder/function/service/directive/controller/endpoint etc.
      
  - Examples:
  
    ```
    (admin-area)
    (merchant-area)
    ([common]CHANGELOG.md)
    ([backend]helpers.js)
    ([admin-area]message-templates)
    ([backend]fnBuildTemplate)
    ([frontend]yashToastr)
    ```
