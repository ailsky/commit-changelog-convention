## Overview CHANGELOG convention

- Format of the `[Unreleased]` section inside CHANGELOG; `(<scope>)` is optional

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

- Allowed `<section>` for CHANGELOG

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
