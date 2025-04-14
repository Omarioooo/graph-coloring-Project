<span style="color:RED; font-weight: Bold; font-size: 35px;"> Data Science Tools Project</span>
___

# 📅 Course Scheduling and Conflict Resolution System
___
___

## 📂 Data Preparation Phase

### 🗃️ Data Loading & Initial Processing
- 📥 Loaded multi-sheet Excel file containing student-course registrations
- 🔄 Processed each department's sheet separately:
  - Added department name as new column (`القسم`)
  - Cleaned department names by stripping whitespace
- 🗑️ Removed unnecessary second column from all sheets
- 🏷️ Standardized column names across all sheets:
  - `القسم` (Department)
  - `رقم الطالب` (Student ID)
  - `اسم الطالب` (Student Name)
  - ... [other columns]

### 🧹 Data Cleaning
- ➕ Combined all sheets into single DataFrame
- 🕳️ Removed null values
- 💾 Exported cleaned data as CSV for further analysis

## 📊 Network Graph Construction

### 🛠️ Graph Components
- 🏗️ Built undirected graph using NetworkX
- ⚙️ Node representation:
  - Each course (`رمز المقرر`) as unique node
- 🔗 Edge representation:
  - Edge between two courses indicates shared students (conflict)

### 📈 Graph Statistics
| Metric | Value |
|--------|-------|
| Number of courses (nodes) | 112 |
| Number of conflicts (edges) | 1,526 | 
| Average degree | 27.25 |
| Maximum degree | 56 |
| Graph density | 0.244 |

## 🔍 Visual Analysis

### 1️⃣ Course Popularity
- 📊 Bar chart showing student count per course
- 🏆 Top courses have 50+ students

### 2️⃣ Conflict Graph Visualization
- 🕸️ Spring layout visualization of entire graph
- 🔴 High-degree courses appear as central hubs

## 🎨 Graph Coloring Solution

### ⏱️ DSATUR Algorithm Implementation
- 🎨 Greedy graph coloring with `DSATUR` strategy
- ⏱️ Processing time: [X] seconds
- 🏆 Results:
  - **Number of exam periods needed:** 9
  - **Color distribution:** [chart]

### 📅 Exam Schedule
| Period | Courses Assigned | Conflict-Free? |
|--------|------------------|----------------|
| 1 | `XXXX`, `XXXX` | ✅✅✅ | 
| 2 | `XXXX`, `XXXX` | ✅✅✅ |
| ... | ... | ... |

## 📊 Final Visualization
- 🖍️ Each color represents separate exam period
- � No adjacent nodes share same color (no conflicts)

## ✅ Validation
- ✔️ Confirmed no student has exams in same period
