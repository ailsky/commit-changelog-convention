# Versioning

## Overview Git commit convention

- Format of the commit message; `(<scope>)` is optional

        <type>(<scope>)[<branch id>]: <subject>
        <BLANK LINE>
        <body>
        <BLANK LINE>
        <footer>

    - Examples:
        
            doc([common]CHANGELOG.md)[13]: Update Unreleased section

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
            ([common]CHANGELOG.md)
            ([backend]helpers.js)
            ([frontend]message-templates)
            ([backend]fnBuildTemplate)
            ([frontend]toastr)

## Overview CHANGELOG.md convention

- Format of the `[Unreleased]` section inside CHANGELOG.md; `(<scope>)` is optional

        # [Unreleased]
        <BLANK LINE>
        ## <trello branch id>
        ### <section>
        - <scope/parent scope>
          - <child scope>
            - description 1
            - description <n>
        <BLANK LINE>
        ## <trello branch id>
        ### <section>
        - <scope/parent scope>
          - <child scope>
            - description 1
            - description <n>
        <BLANK LINE>
        ----
        <BLANK LINE>
        <MAIN CONTENT>

- Allowed `<section>` for CHANGELOG.md

    - **New features**
    - **Bug fixes**
    - **Breaking changes**

- Allowed `<scope>`; `<scope>` is optional

    - **Public**
    - **Backend**
    - **Frontend**
    - **Common**
    -     <parent scope>
            <child scope>

        `<parent scope>` it is any of `<scope>`
        
        `<parent scope>` is required when you use `<child scope>`

        - Allowed `<child scope>`

            `filename/folder/function/service/directive/controller/endpoint etc.`
    
    - Examples:

            - Backend
              - fnBuildTemplate
                - description 1
                - description 2

## Custom configuration

Place `commit-msg-configs` near `commit-msg` (to `.git/hooks`) and override any config from `config area` of `commit-msg`
