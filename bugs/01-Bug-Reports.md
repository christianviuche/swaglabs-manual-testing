# 🐞 Bug Reports: Swag Labs

**Project:** Swag Labs E-Commerce
**Tester:** Christian Andrés Viuche
**Date:** November 2025

---

## 🔴 Bug-001: Product images are broken (dog placeholder) on Inventory page

| Field | Details |
| :--- | :--- |
| **Bug ID** | BUG-INV-001 |
| **Severity** | **High** (User Interface is significantly broken) |
| **Priority** | **High** (Affects product visibility) |
| **Environment** | Google Chrome |
| **Assigned To** | Development Team |

### 📝 Description
When logging in with the `problem_user` account, all product images on the Inventory page fail to load and are replaced with a generic "dog" placeholder image.

### 👣 Steps to Reproduce
1. Navigate to `https://www.saucedemo.com/`
2. Enter username: `problem_user`
3. Enter password: `secret_sauce`
4. Click "Login".
5. Observe the images next to each product.

### ❌ Actual Result
The product images are not displayed. A placeholder image of a dog is shown for every item.

### ✅ Expected Result
The correct image corresponding to each product (Backpack, Bike Light, etc.) should be displayed.

---

## 💥 Bug-002: "Last Name" input overwrites "First Name" field in Checkout

| Field | Details |
| :--- | :--- |
| **Bug ID** | BUG-CHK-002 |
| **Severity** | **Critical** (Blocks user from entering correct shipping info) |
| **Priority** | **High** |
| **Environment** | Google Chrome |
| **User Account** | `problem_user` |

### 📝 Description
In the Checkout: Your Information page, typing into the "Last Name" field does not enter data into that field. Instead, it overwrites the data existing in the "First Name" field.

### 👣 Steps to Reproduce
1. Login as `problem_user`.
2. Add an item to the cart and proceed to "Checkout".
3. In the "First Name" field, enter: `Christian`.
4. Click on the "Last Name" field and attempt to type: `Viuche`.

### ❌ Actual Result
* No text appears in the "Last Name" field.
* The text typed (`Viuche`) overwrites or appends to the "First Name" field incorrectly.
* The user is unable to submit unique values for both fields.

### ✅ Expected Result
The user should be able to enter the Last Name independently without affecting the First Name field.

---

## 🟡 Bug-003: Sort dropdown selection resets immediately (Stuck on "A to Z")

| Field | Details |
| :--- | :--- |
| **Bug ID** | BUG-INV-003 |
| **Severity** | **Medium** (Core feature unusable) |
| **Priority** | **Medium** |
| **Environment** | Google Chrome |
| **User Account** | `problem_user` |

### 📝 Description
The product sort dropdown on the Inventory page is non-functional. When a user attempts to select a different sorting option (e.g., "Price (low to high)"), the selection is ignored, and the dropdown reverts immediately to the default "Name (A to Z)".

### 👣 Steps to Reproduce
1. Login as `problem_user`.
2. Click the filter dropdown menu (top right).
3. Click on the option "Price (low to high)".
4. Observe the dropdown field value and the product list.

### ❌ Actual Result
* The dropdown value does not update; it remains displaying "Name (A to Z)".
* The product list does not reorder.

### ✅ Expected Result
The dropdown should display the selected option ("Price (low to high)"), and the product list should reorder accordingly.
