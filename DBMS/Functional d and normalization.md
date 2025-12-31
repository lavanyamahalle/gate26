For **any number of 1s** in **3 spots**:

### ✅ **Formula**

[
\boxed{2^n}
]

where
( n = ) number of spots

### 👉 For 3 spots:

[
\boxed{2^3 = 8}
]

### **All possible combinations**

```
000
001
010
011
100
101
110
111
```

✔️ This includes **0 ones, 1 one, 2 ones, and 3 ones**.


<br>

**Question: How many superkeys?**

### ✅ **Standard DBMS Formula**

If a relation has:

* **n = total attributes**
* **k = attributes in a (single) candidate key**

Then,

[
\boxed{\text{Number of superkeys} = 2^{(n-k)}}
]

### 🔍 **Why?**

* A **superkey** = candidate key **+ any subset** of remaining attributes
* Remaining attributes = ( n - k )
* Number of subsets = ( 2^{(n-k)} )

### ✏️ **Example**

If

* Total attributes ( n = 5 )
* Candidate key size ( k = 2 )

[
\text{Superkeys} = 2^{(5-2)} = 2^3 = \boxed{8}
]

⚠️ **Note (Exam Tip):**
This formula is valid when there is **only one candidate key** (most exam questions assume this).

<br>
**Question: How many superkeys?**

### ✅ **Standard DBMS Formula**

If a relation has:

* **n = total attributes**
* **k = attributes in a (single) candidate key**

Then,

[
\boxed{\text{Number of superkeys} = 2^{(n-k)}}
]

### 🔍 **Why?**

* A **superkey** = candidate key **+ any subset** of remaining attributes
* Remaining attributes = ( n - k )
* Number of subsets = ( 2^{(n-k)} )

### ✏️ **Example**

If

* Total attributes ( n = 5 )
* Candidate key size ( k = 2 )

[
\text{Superkeys} = 2^{(5-2)} = 2^3 = \boxed{8}
]

⚠️ **Note (Exam Tip):**
This formula is valid when there is **only one candidate key** (most exam questions assume this).

If you want, tell me **n and k**, I’ll calculate instantly.
<br>
**According to the formula (DBMS):**

### 🔹 Formula

[
\boxed{\text{Number of superkeys} = 2^{(n-k)}}
]

where

* ( n ) = total attributes
* ( k ) = attributes in **one candidate key**

---

### 🔹 Apply to your question

Relation: **ABCD** → ( n = 4 )

From
A → B, B → C, C → A

Candidate keys: **AD, BD, CD**
Size of each candidate key = **2** → ( k = 2 )

---

### 🔹 Calculation

[
2^{(4-2)} = 2^2 = \boxed{4}
]

---

### ⚠️ Important exam note

This formula assumes **only ONE candidate key**.
Since here we have **3 candidate keys**, the formula **cannot be directly used**.

👉 **Correct number of superkeys (by concept)** = **7**

---

### ✨ Exam-ready line

> According to the formula, number of superkeys = (2^{(n-k)} = 4), but since multiple candidate keys exist, the actual number of superkeys is **7**.
<br>

### ✅ **FINAL EXAM NOTE: How to Calculate Candidate Keys & Superkeys (DBMS)**



### 🧠 **Short trick**

* Attributes **not appearing on RHS of any FD** → must be in every candidate key.
* If attributes determine each other (A→B, B→C, C→A), **any one is enough**.

---

### 📌 **Example**

FDs: A→B, B→C, C→A
Relation: ABCD

* D not on RHS → must be included
* Any one of {A, B, C} + D is enough

👉 **Candidate Keys:**
[
\boxed{AD,; BD,; CD}
]

---

## 🔐 **B) How to Find Superkeys**

### **Definition**

> Any attribute set that **contains a candidate key**.

---

### **Method 1: Conceptual (Always Correct)**

1. List all candidate keys
2. Add any extra attributes
3. Every superset is a superkey

✔️ Use this when **multiple candidate keys exist**

---

### **Method 2: Formula (Exam-Fast Method)**

[
\boxed{\text{Number of superkeys} = 2^{(n-k)}}
]

where

* ( n ) = total attributes
* ( k ) = size of **one** candidate key

⚠️ **Only valid when there is ONE candidate key**

---

### 📌 **Example (Your case)**

ABCD, candidate keys = AD, BD, CD

* All superkeys must include **D**
* And at least one of {A, B, C}

[
\text{Superkeys} = 7
]

---

## 🧠 **Memory Trick (Perfect for Exam)**

> **Candidate key = minimal + full coverage**
> **Superkey = candidate key + anything**

