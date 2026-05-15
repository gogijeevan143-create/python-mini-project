# 🐍 Python Mini Project

A set of three Python programs covering core concepts taught in class.

---

## 📚 Topics Covered

`Variables` · `Data Types` · `List / Set / Tuple / Dict` · `Conditionals` · `Loops` · `Functions` · `Default Parameters` · `Mutable vs Immutable`

---

## 📁 Files

| File | Question | Difficulty |
|------|----------|------------|
| `q1_result_analyzer.py` | Student Result Analyzer | 🟢 Easy |
| `q2_library_system.py` | Library Book Management System | 🟡 Medium |
| `q3_shopping_cart.py` | Shopping Cart — Default & Mutable Pitfall | 🔴 Hard |

---

## 📝 Question Summaries

### Q1 — Student Result Analyzer
- Stores student name, roll number, and marks for 5 subjects
- Calculates total and average marks
- Assigns a grade (A / B / C / D / Fail) based on average
- Identifies subjects where the student scored below 40
- All logic wrapped inside `analyze_result(name, roll, marks)`

**Sample Output:**
```
Student: Aarav (Roll: 101)
Total: 340.0, Average: 68.0
Grade: C
Subjects below 40: Subject 2
```

---

### Q2 — Library Book Management System
Demonstrates choosing the **right data structure** for each requirement:

| Structure | Purpose | Reason |
|-----------|---------|--------|
| `dict` | Book catalog | Fast O(1) lookup by book ID |
| `tuple` | Book details | Immutable — title/author/year shouldn't change |
| `list` | Borrowed books | Preserves insertion order |
| `set` | Member IDs | Automatically prevents duplicates |

**Functions implemented:**
- `add_book()` — add a book to the catalog
- `borrow_book()` — issue a book (with validation)
- `return_book()` — return a borrowed book
- `register_member()` — register a member (ignores duplicates silently)
- `show_available()` — display books currently not borrowed

---

### Q3 — Shopping Cart (Mutable Default Pitfall)

**Part A — Spot the Bug**
Explains why `def add_item(item, cart=[])` is dangerous — the list default is shared across all calls.

**Part B — Fix It**
Corrects the bug using `cart=None` as a sentinel default.

**Part C — Full Shopping Cart**
- `create_cart(owner, discount=0)` — creates an independent cart per customer
- `add_to_cart(cart, name, price, qty=1)` — adds items
- `update_price(price_tuple, new_price)` — demonstrates `TypeError` on tuple mutation
- `calculate_total(cart)` — computes total with discount applied

**Discussion answers** (written as comments inside the file):
1. Why `discount=0` is safe but `cart=[]` is dangerous
2. Rebinding vs mutating
3. Which types are mutable — `list`, `dict`, `set` ✅ vs `tuple`, `str`, `int` ❌
4. Why list modifications inside a function reflect outside (pass-by-reference)

---

## ▶️ How to Run

Make sure Python 3 is installed, then run any file from the terminal:

```bash
python q1_result_analyzer.py
python q2_library_system.py
python q3_shopping_cart.py
```

---

## 👤 Author

**Your Name**
- GitHub: [@your-username](https://github.com/your-username)
