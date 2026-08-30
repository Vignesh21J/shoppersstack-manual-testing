# ShoppersStack — Manual Testing Project

Manual functional testing of the **ShoppersStack e-commerce web application**, executed end-to-end using **Agile Scrum methodology** across 4 sprints.

## Project Summary

| Metric | Result |
|---|---|
| Test Cases Designed & Executed | **219** |
| Requirement Coverage (RTM) | **13 / 13 Product Backlog items (100%)** |
| Defects Logged | **20** (1 Blocker, 1 Critical, 12 Major, 1 Medium, 5 Minor) |
| Test Types Covered | Functional, Negative, Boundary Value, Edge Case |
| Sprints | 4 |

## Scope

- Admin / Merchant / Shopper Signup & Login
- Product Search & Category Browsing
- Add to Cart & Buy a Product
- Delivery Address Management (with pincode serviceability)
- Order Placement — Cash on Delivery, Net Banking, Debit Card, Credit Card
- Voucher Generation, View Coupons, and Redemption at Checkout

## Key Findings

- **BUG-001 (Blocker)** — Merchant Signup's "Finish" button has no bound submit handler; no Merchant account can ever be created, blocking all downstream Merchant testing.
- **BUG-016 (Critical)** — Voucher access login accepts incorrect credentials (both wrong email and wrong password), allowing unauthenticated access to the Coupon Generator.
- **BUG-014 (Major)** — Addresses with non-serviceable pincodes are saved silently with no warning, risking undeliverable orders.
- **BUG-017 (Major)** — View Coupons search does not filter results at all.

Full details in `04-Defect-Report.xlsx`.

## Repository Structure

```
shoppersstack-manual-testing/
├── 01-Test-Plan.docx                  # Scope, approach, entry/exit criteria, environment
├── 02-Test-Scenarios-TestCases.xlsx   # 219 test cases with execution results & dashboard
├── 03-RTM.xlsx                        # Requirement Traceability Matrix (13/13 coverage)
├── 04-Defect-Report.xlsx              # All 20 defects, severity-classified
├── 05-Test-Execution-Summary.docx     # Final results report with findings & recommendations
└── README.md
```

## Methodology

Testing followed Agile Scrum: a Product Backlog of 13 user stories was broken into 4 sprints, each covering a related set of modules. For every module, test scenarios were derived from the requirement document, then broken into detailed test cases across four categories — functional, negative, boundary value, and edge case — before execution and defect logging.

| Sprint | Modules |
|---|---|
| 1 | Admin / Merchant / Shopper Signup & Login |
| 2 | Search Product, Add to Cart, Buy a Product |
| 3 | Add Delivery Address, Place Order (4 payment methods) |
| 4 | Voucher Generation, View Coupons, Redeem Coupon |

## Tools Used

- Microsoft Excel — test design, execution tracking, defect logging
- Browser DevTools (Console / Network) — defect root-cause verification
- Git / GitHub — version control and project delivery

## Author

**Vignesh J** — Manual Test Engineer (Aspiring SDET)
