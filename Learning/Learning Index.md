# 📚 Learning Index 📚


<!-- "The MIT License (MIT) Copyright © 2025 Jaroslaw Ladosz" -->


**📝 Purpose:**  
This file is your own **central hub for learning**:

- ➕ **Create new notes** with custom titles
    
- 📄 **Browse previously created notes** in an organized table
    
- 🔖 **Quickly see tags and types** for each note
---
✨📘✨📗✨📙✨📖✨📚✨📖✨📙✨📗✨📘✨

---
## ➕ Create a new strategy topic ➕
```button
name ➕ New Strategy
type command
action QuickAdd: NewStrategy
```
---
## ➕ Create a new keyword topic ➕
```button
name ➕ New Keyword
type command
action QuickAdd: NewKeyword
```
---
## ➕ Create a new mindset topic ➕
```button
name ➕ New Mindset
type command
action QuickAdd: NewMindset
```
---
## 📒 Table of learned content 📒
```dataview
table file.name as "Topic",
choice(
  contains(file.folder, "01-ST"), "📚 Strategy",
  choice(
    contains(file.folder, "02-KW"), "🔑 Keyword",
    choice(
      contains(file.folder, "03-MS"), "💡 Mindset",
      "Other"
    )
  )
) as "Type",
file.tags as "Tags",
 date_created as "Date Created",
file.mtime as "Last Modified"
from "Learning/01-ST" or "Learning/02-KW" or "Learning/03-MS"
sort file.name asc
```
---
Detailed View

---
## 📄 All Learning Notes

### 📚 Strategies
```dataview
table file.name as "Topic", file.tags as "Tags", date_created as "Date Created", file.mtime as "Last Modified"
from "Learning/01-ST"
sort file.name asc

```
### 🔑 Keywords
```dataview
table file.name as "Topic", file.tags as "Tags", date_created as "Date Created", file.mtime as "Last Modified"
from "Learning/02-KW"
sort file.name asc

```


### 💡 Mindsets

```dataview
table file.name as "Topic", file.tags as "Tags", date_created as "Date Created", file.mtime as "Last Modified"
from "Learning/03-MS"
sort file.name asc

```
## 📜 License  
Licensed under the [MIT License](./LICENSE) © 2025 Jaroslaw Ladosz
