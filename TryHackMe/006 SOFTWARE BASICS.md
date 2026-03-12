
# Module: Software Basics

## Topics
- Data Representation
- Data Encoding
- Python: Simple Demo
- JavaScript: Simple Demo
- Database SQL Basics

---

## Objective
The goal of this module is to understand how computers store and interpret data at the lowest level from binary and hex all the way up to how programming languages like Python and JavaScript work, and how databases store and retrieve information using SQL.

---

## Key Concepts

### Data Representation
- Computers only understand two things: **0** and **1** — these are called **bits** (binary digits).
- Everything stored in a computer — numbers, text, images, video is ultimately just a series of 0s and 1s.
- **Number Systems:**

| System | Base | Digits Used | Example |
|--------|------|-------------|---------|
| Binary | 2 | 0, 1 | `1010` = 10 in decimal |
| Decimal | 10 | 0–9 | `10` |
| Hexadecimal | 16 | 0–9, A–F | `0xA` = 10 in decimal |

- **Bits and Bytes:**
  - 1 bit = a single 0 or 1
  - 8 bits = 1 byte
  - 1 byte can represent 256 different values (0–255)
- **Colors** are represented using RGB values — three numbers (Red, Green, Blue) each ranging from 0 to 255. For example, pure red is `RGB(255, 0, 0)`.
- Hexadecimal is preferred by programmers because it's more compact and easier to read than long binary strings.

### Data Encoding
- If everything is just numbers, how does a computer know that `01010100` means the letter **T**? The answer is **encoding** — an agreed-upon standard that maps numbers to characters.
- **ASCII** — the original character encoding standard. It uses 7 bits to represent 128 characters (English letters, digits, punctuation). For example, `T` = `01010100` in binary = `54` in hex.
- **Unicode** — an expanded standard that supports virtually every language and symbol in the world, including emojis.
- **UTF-8** — the most widely used implementation of Unicode. It's backward-compatible with ASCII and uses variable-length encoding to be efficient.

**Example — How "TryHackMe" is stored:**

| Character | Hex |
|-----------|-----|
| T | 54 |
| r | 72 |
| y | 79 |
| H | 48 |
| a | 61 |
| c | 63 |
| k | 6b |
| M | 4d |
| e | 65 |

- **Why this matters in cybersecurity:** Attackers exploit encoding in attacks like path traversal (`../` encoded as `%2e%2e%2f`) and SQL injection (encoding malicious queries to bypass filters).

### Python: Simple Demo
- **Python** is a high-level, general-purpose programming language — popular for everything from automation scripts and web apps to data science and cybersecurity tools.
- "High-level" means Python hides the complex low-level details, making it easier to read and write.
- Key Python concepts used in the demo:

| Concept | Description | Example |
|---------|-------------|---------|
| Variable | Stores a value in memory | `secret = 10` |
| Input | Gets text from the user | `guess = input("Take a guess: ")` |
| Type conversion | Converts text to a number | `guess = int(text)` |
| Conditional | Checks if something is true | `if guess < secret:` |
| Loop | Repeats until a condition is met | `while guess != secret:` |
| Import | Loads a module for extra tools | `import random` |

**Python Guess the Number Game (simplified):**
```python
import random

secret = random.randint(1, 20)
tries = 0
guess = 0

print("I'm thinking of a number between 1 and 20")

while guess != secret:
    text = input("Take a guess: ")
    guess = int(text)
    tries += 1
    if guess < secret:
        print("Too low, try again.")
    elif guess > secret:
        print("Too high, try again.")

print(f"You got it in {tries} tries!")
```

### JavaScript: Simple Demo
- **JavaScript** is the language of the web — it runs inside your browser and makes websites interactive.
- With **Node.js**, JavaScript can also run on the server side, making it a full stack language.
- JavaScript and Python are similar in logic but different in syntax. Comparing the two side-by-side is a great way to understand how programming languages differ.

| Concept | Python Syntax | JavaScript Syntax |
|---------|--------------|-------------------|
| Variable | `secret = 10` | `let secret = 10;` |
| Print | `print("Hello")` | `console.log("Hello");` |
| User Input | `input("Guess: ")` | `readline` (via Node.js) |
| If statement | `if guess < secret:` | `if (guess < secret) {` |
| Loop | `while guess != secret:` | `while (guess !== secret) {` |

**JavaScript Guess the Number Game (simplified ver):**
```javascript 
const secret = Math.floor(Math.random() * 20) + 1;
let tries = 0;
let guess = 0;

console.log("I'm thinking of a number between 1 and 20");

while (guess !== secret) {
    const text = prompt("Take a guess: ");
    guess = parseInt(text);
    tries++;
    if (guess < secret) {
        console.log("Too low, try again.");
    } else if (guess > secret) {
        console.log("Too high, try again.");
    }
}

console.log(`You got it in ${tries} tries!`);
```

### Database SQL Basics
- A **database** is an organized collection of data. Think of it like a structured spreadsheet that can be queried and managed efficiently.
- **Relational databases** store data in tables made up of rows and columns. Each table represents one type of data (e.g. users, products, orders).
- **SQL (Structured Query Language)** is the language used to communicate with relational databases.
- Common SQL commands:

| Command | What It Does | Example |
|---------|-------------|---------|
| `SELECT` | Retrieve data | `SELECT * FROM users;` |
| `WHERE` | Filter results | `SELECT * FROM users WHERE id = 1;` |
| `INSERT INTO` | Add new data | `INSERT INTO users VALUES ('Alice', 25);` |
| `UPDATE` | Modify existing data | `UPDATE users SET age = 26 WHERE name = 'Alice';` |
| `DELETE` | Remove data | `DELETE FROM users WHERE name = 'Alice';` |
| `CREATE TABLE` | Create a new table | `CREATE TABLE users (id INT, name TEXT);` |

- **Primary Key** — a unique identifier for each row in a table (like a student ID).
- **Foreign Key** — links one table to another (e.g. an `author_id` in a Books table pointing to the Authors table).
- **Why SQL matters in cybersecurity:** SQL injection is one of the most common web attacks. If user input isn't properly sanitised, attackers can inject malicious SQL queries to read, modify, or delete database contents.

---

## Activity / What I Did

This module covered five connected rooms, each building on the last — starting from raw binary data all the way up to full database queries.

- **Data Representation** — I worked through exercises converting numbers between binary, decimal, and hexadecimal. I also learned how colors are stored as RGB values and practiced converting hex color codes.

- **Data Encoding** — I explored how the ASCII and Unicode standards map numbers to characters. I used a static site provided in the room to see how text is stored in binary and hex for example, seeing "TryHackMe" broken down character by character into hex values.

- **Python: Simple Demo** — I ran and modified a "Guess the Number" game inside an attached VM. I edited the script step by step: first making it pick a random number, then reading user input, then adding feedback (too high / too low), and finally adding a loop to keep playing until the user wins.

```bash
cd /home/ubuntu/Python-Demo
python3 guess_v1.py   # Basic version
python3 guess_v3.py   # Full version with loop and feedback
```

- **JavaScript: Simple Demo** — I did the same "Guess the Number" game but written in JavaScript, running it via Node.js. Comparing the two versions side by side made it really clear how the two languages differ in syntax while doing the exact same thing.

```bash
cd /home/ubuntu/JavaScript-Demo
node guess_v1.js   # Basic version
node guess_v3.js   # Full version with loop and feedback
```

- **Database SQL Basics** — I practiced writing SQL queries against a live database inside a VM selecting records, filtering with `WHERE`, inserting new rows, and updating existing data.

```sql
SELECT * FROM users;
SELECT * FROM users WHERE username = 'admin';
INSERT INTO users (username, password) VALUES ('alice', 'pass123');
UPDATE users SET password = 'newpass' WHERE username = 'alice';
DELETE FROM users WHERE username = 'alice';
```

---

## What I Learned

This module completely changed how I think about data and also the most time consuming write ups i ever write. The Data Representation and Encoding rooms made that very concrete and drain. The Python and JavaScript rooms were genuinely fun I liked that both languages were used to build the same game, because it made it easy to compare them without getting lost in what the code was actually doing. Seeing how little it takes to write a working program was actually motivating. The SQL room was probably the most directly useful from a security standpoint understanding how databases work and what SQL injection looks like at the query level makes a lot of cybersecurity concepts click into place. So yaah
