## 📦 Linux Data Handling: Commands & Tutorials

---

## 📖 1️⃣ Text & File Data Handling Commands

| Command | Purpose                             | Example                           |        |
| :------ | :---------------------------------- | :-------------------------------- | ------ |
| `cat`   | View contents of a file             | `cat data.txt`                    |        |
| `head`  | View first N lines                  | `head -n 10 data.txt`             |        |
| `tail`  | View last N lines                   | `tail -n 20 logs.txt`             |        |
| `cut`   | Extract columns/fields              | `cut -d',' -f2 data.csv`          |        |
| `awk`   | Pattern scanning & processing       | `awk -F',' '{print $2}' data.csv` |        |
| `sed`   | Stream editor for filtering/editing | `sed 's/foo/bar/g' file.txt`      |        |
| `sort`  | Sort data                           | `sort names.txt`                  |        |
| `uniq`  | Remove duplicates                   | \`sort data.txt                   | uniq\` |
| `wc`    | Count lines, words, characters      | `wc -l file.txt`                  |        |
| `tr`    | Translate/replace/delete characters | `tr 'a-z' 'A-Z' < file.txt`       |        |
| `paste` | Merge files line-by-line            | `paste file1.txt file2.txt`       |        |
| `join`  | Join files based on a common field  | `join file1.txt file2.txt`        |        |

---

## 📊 2️⃣ Data Handling Tutorials

### 📌 Tutorial 1: Extract Specific Columns from CSV

```bash
cat data.csv
```

```
Name,Age,City
Atul,30,Mumbai
Ravi,28,Pune
```

👉 Extract names:

```bash
cut -d',' -f1 data.csv
```

👉 Extract names and cities:

```bash
awk -F',' '{print $1, $3}' data.csv
```

---

### 📌 Tutorial 2: Replace Text in a File

Replace all occurrences of `Dev` with `Developer` in `file.txt`

```bash
sed 's/Dev/Developer/g' file.txt
```

---

### 📌 Tutorial 3: Sort and Remove Duplicate Lines

```bash
sort names.txt | uniq
```

---

### 📌 Tutorial 4: Count Lines, Words, Characters

```bash
wc -l file.txt      # Line count  
wc -w file.txt      # Word count  
wc -c file.txt      # Character count  
```

---

### 📌 Tutorial 5: Combine Two Files Line-by-Line

```bash
paste file1.txt file2.txt
```

---

## 📈 3️⃣ Bonus: Data Search & Filtering

| Command | Purpose                  | Example                    |                   |
| :------ | :----------------------- | :------------------------- | ----------------- |
| `grep`  | Search text by pattern   | `grep "Atul" names.txt`    |                   |
| `egrep` | Extended regex support   | \`egrep "Atul              | Ravi" names.txt\` |
| `find`  | Locate files/directories | `find /home -name "*.log"` |                   |
| `xargs` | Pass output as arguments | \`find . -name "\*.log"    | xargs rm -f\`     |

---

## 📝 4️⃣ Data Handling Example: Log Analysis

👉 Find top 10 IP addresses in a web server log

```bash
awk '{print $1}' access.log | sort | uniq -c | sort -nr | head -n 10
```

👉 Count occurrences of HTTP 500 errors

```bash
grep "500" access.log | wc -l
```

---

## 📚 5️⃣ Recommended Practice Exercises

* 📄 Extract emails from a file
* 📄 Find top 5 largest files in `/var/log`
* 📄 Count how many lines contain the word `error`
* 📄 Replace all occurrences of `production` with `prod` in a config file
* 📄 Sort a CSV file based on the second column

---

## 📦 Wrap-up

Linux CLI is immensely powerful for data handling — whether for text manipulation, logs analysis, or data preparation for scripts and automation.

