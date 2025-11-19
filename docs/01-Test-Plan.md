# 📄 Test Plan: Swag Labs (SauceDemo) E-Commerce

| Project Name | Swag Labs E-Commerce Testing |
| :--- | :--- |
| **Version** | 1.0 |
| **Author** | Christian Andrés Viuche |
| **Date** | November 2025 |
| **Status** | Draft |

---

## 1. Introduction
The objective of this Test Plan is to define the strategy, scope, and approach for testing the **Swag Labs (SauceDemo)** e-commerce website. This application allows users to browse products, add them to a cart, and complete a checkout process.

**Target URL:** [https://www.saucedemo.com/](https://www.saucedemo.com/)

## 2. Objectives
* Verify that the critical user flows (Login -> Shop -> Checkout) work correctly.
* Ensure the UI is consistent across different browsers (Chrome, Safari).
* Identify and report functional defects before the "release."

## 3. Scope (Alcance)

### ✅ In Scope (What we WILL test)
* **Authentication:** Login with valid, locked_out, and invalid users.
* **Inventory:** Viewing products, sorting (A-Z, Price), and product details.
* **Cart Functionality:** Adding/removing items, cart persistence.
* **Checkout Flow:** Entering shipping info, verifying totals, and completing the order.
* **Logout:** Successfully ending the session.

### ❌ Out of Scope (What we will NOT test)
* **Performance Testing:** Load testing or stress testing is not required for this cycle.
* **Security Testing:** No penetration testing or vulnerability scanning.
* **Mobile App:** We are strictly testing the *web* version.

## 4. Test Strategy

We will perform **Black Box Testing** using a manual approach.

* **Functional Testing:** Validating all features against expected behavior.
* **Smoke Testing:** A quick run of the critical path (Login + Buy 1 item) to ensure stability.
* **Compatibility Testing:** Checking the site on Google Chrome and one mobile browser (via DevTools).

## 5. Test Environment

| Component | Details |
| :--- | :--- |
| **URL** | `https://www.saucedemo.com/` |
| **Browsers** | Google Chrome (Latest), Firefox (Latest) |
| **OS** | Windows 10/11 or macOS |
| **Test Data** | Standard User: `standard_user` <br> Locked User: `locked_out_user` <br> Password: `secret_sauce` |

## 6. Deliverables
By the end of this project, we will provide:
1.  **Test Plan** (This document).
2.  **Test Cases Suite** (Detailed steps for every test).
3.  **Bug Reports** (Documented defects found during execution).
