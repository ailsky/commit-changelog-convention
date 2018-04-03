# Commit message examples:

```
docs([common]CHANGELOG)[13]: update Unreleased section
```

```
fix(frontend)[15]: remove debug info for the most benefit coupon
- [frontend]app/bounce-modules/invoices/invoices.js
  - remove debug info for the most benefit coupon
```

```
feat(backend)[41]: remove extra checks in fnCheckCouponLoyaltyRulesCompletion function
- [backend]server/utils/helpers/helpers.js
  - remove extra checks in `fnCheckCouponLoyaltyRulesCompletion` function on publish wallet's review about company by `Admin`
```

```
feat(backend)[41]: add handling for reviewed type of loyalty program to helpers
- [backend]server/hooks/client-rating-model.js
  - add after save hook to watch company reviews changes
- [backend]server/remotes/invoice.js
  - add sType argument for `fnCheckCouponLoyaltyRulesCompletion` function call
- [backend]server/utils/helpers/helpers.js
  - add `reviewed` type of loyalty program handling to `fnCheckCouponLoyaltyRulesCompletion`
```

```
feat[42]: add ability publish/unpublish ratings
- backend
  - add new field `public` model to `ClientRating` and to `ItemRating`
  - add new methods `publish`, `unpublish` to `ClientRating`, `ItemRating` with is allowed only for admins and can change state of ratings
  - add new methods `public`, `publicCount` to `ClientRating`, `ItemRating` models witch return published and own ratings
- frontend
  - add info `Your reviews and votes will be accounted for rating and visible for other when administrator approves it`
- [frontend]admin-area
  - add new routs `reviews/client-list`, `reviews/items-list`

BREAKING CHANGE: changed ACLs of methods
  - methods `find` and `count` of `ClientRating` and `ItemRating` are allowed only for admins
```

```
feat[44]: add ability to apply coupons for Client.markAsPaid
- backend
  - add new endpoint `Client.calcDiscount`
  - add ability to use `Coupon` for `Client.markAsPaid`
  - add new field `embeddedCoupons` to `Invoice` which stores coupons applied by Merchant
- frontend
  - update views of invoices at all areas - add compatibility with coupons applied via `Client.markAsPaid`

BREAKING CHANGE: deprecated a lot of methods, deprecated models
- field `embededItems` renamed to `embeddedItems`
- changed endpoint `Client.markAsPaid` signaturey
```
