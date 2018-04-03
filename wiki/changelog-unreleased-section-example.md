# Example of the [Unreleased] section inside CHANGELOG

```
# [Unreleased]

## 1
### New features
- Admin area
  - messages-templates
    - Add length verification for template subject, body and custom event label fields
    - Add new checkbox control for select notifications wich user cannot disable
    - Add new textinput for custom event label
    - Add new directive for custom checkbox
### Bug fixes
- Admin area
  - messages-templates
    - update validation alerts for subject, body, custom event label
    - change alert style from fixed message box to toaster
    - fix custom event field validation

## 4
### New features
- Add new model 'InvoiceMessage' with validation, which exposed via REST
- Frontend
  - Add new directive 'modDtvs.yashCorrInvoice' which allow to use messages at any area for any invoice
  - Add messages to Invoice details
- Admin area
  - Add messages to Invoice details
- Merchant area
  - Add messages to Invoice details
- Wallet area
  - Add messages to Invoice details

----

# [Released]

## 0.0.1 - 2017-04-17
### New Features
- This CHANGELOG file to hopefully serve as an evolving example of a standardized open source project CHANGELOG.
```
