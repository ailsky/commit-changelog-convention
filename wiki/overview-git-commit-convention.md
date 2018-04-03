# Overview Git commit convention

- Format of the commit message; `(<scope>)` is optional

        <type>(<scope>)[<branch id>]: <subject>
        <BLANK LINE>
        <body>
        <BLANK LINE>
        <footer>

    - Examples:
        
            doc([common]CHANGELOG)[13]: Update Unreleased section

        ---

            feat(frontend)[13]: add fnCleanHTML

                - description
                - description

- Allowed `<type>`; configurable

    - **feat** (feature)
    - **fix** (bug fix)
    - **docs** (documentation)
    - **style** (formatting, missing semi colons, …)
    - **refactor**
    - **test** (when adding missing tests)
    - **chore** (maintain)
  
- Allowed `<scope>`; configurable; `(<scope>)` is optional

    - **public**
    - **backend**
    - **frontend**
    - **common**
    - `<[<parent scope>]<child scope>>`

        `<parent scope>` it is any of `<scope>`
    
        `<parent scope>` is required when you use `<child scope>`
    
    - Allowed `<child scope>`

        - filename/folder/function/service/directive/controller/endpoint etc.

    - Examples:

            (public)
            (backend)
            ([common]CHANGELOG)
            ([backend]helpers.js)
            ([frontend]message-templates)
            ([backend]fnBuildTemplate)
            ([frontend]toastr)
