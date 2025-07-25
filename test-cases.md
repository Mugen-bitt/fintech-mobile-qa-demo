# Test Cases — Fintech Mobile App

---

### TC-01: Successful Loan Issuance
**Preconditions:** User is logged in and has available credit limit  
**Steps:**
1. Go to loan screen
2. Select amount 5,000 ₽
3. Set term to 14 days
4. Click “Get Loan”
5. Confirm action

**Expected Result:** Loan is issued, balance updated, success message shown

---

### TC-02: Loan Extension
**Preconditions:** Active loan exists  
**Steps:**
1. Go to loan details
2. Click “Extend”
3. Confirm extension

**Expected Result:** New due date displayed, interest recalculated

---

### TC-03: Full Loan Repayment
**Preconditions:** Active loan exists, positive account balance  
**Steps:**
1. Go to loan screen
2. Click “Repay”
3. Choose method
4. Confirm payment

**Expected Result:** Balance updated, loan marked as closed

---

### TC-04: Attempt to Get Loan with Zero Amount
**Preconditions:** User logged in  
**Steps:**
1. Set loan amount slider to 0 ₽
2. Try to proceed

**Expected Result:** Error or validation message, loan not issued

---

### TC-05: API — GET /loan/status
**Steps:**
1. Send GET request with valid token

**Expected Result:** 200 OK, JSON includes loan_id, status, amount, due_date

---

### TC-06: Analytics Event — loan_success
**Preconditions:** User completes loan issuance  
**Steps:**
1. Complete TC-01  
2. Capture network traffic (e.g., Charles)

**Expected Result:** Event `loan_success` is sent with correct parameters

---

### TC-07: Localization — Chinese Market
**Steps:**
1. Switch app to Chinese locale
2. Open loan and repayment screens

**Expected Result:** Currency = ¥, date/number format match locale, UI not broken
