
# 📋 Test Cases Suite: Swag Labs

* **Project:** Swag Labs E-Commerce
* **Module:** Main Functionality
* **Author:** Christian Andrés Viuche

---

## 1. Authentication Module 🔐

| ID | Test Summary | Preconditions | Test Data | Steps | Expected Result |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **TC-AUTH-01** | **Verify successful login with valid credentials** | User is on the Login Page | User: `standard_user`<br>Pass: `secret_sauce` | 1. Enter username.<br>2. Enter password.<br>3. Click "Login". | User is redirected to the "Products" page (Inventory). |
| **TC-AUTH-02** | **Verify error message for locked out user** | User is on the Login Page | User: `locked_out_user`<br>Pass: `secret_sauce` | 1. Enter username.<br>2. Enter password.<br>3. Click "Login". | User remains on Login page. Error message displayed: *"Epic sadface: Sorry, this user has been locked out."* |
| **TC-AUTH-03** | **Verify error message for invalid password** | User is on the Login Page | User: `standard_user`<br>Pass: `wrong_pass` | 1. Enter username.<br>2. Enter invalid password.<br>3. Click "Login". | Error message displayed: *"Epic sadface: Username and password do not match any user in this service"* |

---

## 2. Inventory & Cart Module 🛒

| ID | Test Summary | Preconditions | Test Data | Steps | Expected Result |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **TC-CART-01** | **Add a single item to the cart** | User is logged in | Item: "Sauce Labs Backpack" | 1. Locate "Sauce Labs Backpack".<br>2. Click "Add to cart". | Button changes to "Remove". Cart badge shows "1". |
| **TC-CART-02** | **Sort products by Price (Low to High)** | User is logged in | N/A | 1. Click the sort dropdown (top right).<br>2. Select "Price (low to high)". | The first item is "Sauce Labs Onesie" ($7.99). The last item is "Sauce Labs Fleece Jacket" ($49.99). |

---

## 3. Checkout Module (End-to-End) 💳

| ID | Test Summary | Preconditions | Test Data | Steps | Expected Result |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **TC-E2E-01** | **Verify successful checkout process** | User is logged in and has 1 item in cart | First: `Andres`<br>Last: `Madroñero`<br>Zip: `180001` | 1. Click Cart icon.<br>2. Click "Checkout".<br>3. Fill in First Name, Last Name, Zip.<br>4. Click "Continue".<br>5. Click "Finish". | User is redirected to "Checkout: Complete!" page. Message *"Thank you for your order!"* is displayed. |
