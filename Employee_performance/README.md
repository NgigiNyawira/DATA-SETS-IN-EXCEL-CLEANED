#  Employee Performance Analytics — Excel Dashboard Project

![Excel](https://img.shields.io/badge/Tool-Microsoft%20Excel-217346?style=flat&logo=microsoft-excel&logoColor=white)
![Records](https://img.shields.io/badge/Employees-876-blue?style=flat)
![Departments](https://img.shields.io/badge/Departments-6-orange?style=flat)
![Locations](https://img.shields.io/badge/Offices-6%20Global-purple?style=flat)
![Status](https://img.shields.io/badge/Status-Complete-brightgreen?style=flat)

A comprehensive HR analytics dataset covering employee demographics, compensation, performance scores, project involvement, and training — built for multi-dimensional workforce analysis and an interactive Excel dashboard.

---

## Dashboard Preview

> The workbook includes a fully built **interactive Dashboard** sheet with KPI cards and charts covering headcount, salary, performance, bonuses, and remote work breakdowns by department.

---

##  File Structure

The workbook (`employee_performance.xlsx`) contains **14 sheets**:

| Sheet | Description |
|---|---|
| `ORIGINAL` | Raw cleaned dataset — 876 employees × 21 columns |
| `MULTIPLE` | Multi-variable analysis combining key HR dimensions |
| `HEADCOUNT` | Employee count breakdown by department |
| `AVRG SALARY DEPT` | Average salary per department |
| `PERFORM PER DEPT` | Average performance score per department |
| `SALARY IN DEPT` | Salary distribution by department and marital status |
| `AVRG WORK EXP` | Average years of work experience by department |
| `PROJECT COUNT` | Project count distribution across departments |
| `AVRG FEEDBACK` | Average manager feedback score by remote work status |
| `TOTAL BONUS` | Total bonus pool breakdown by department and category |
| `REMOTE AVRG` | Average metrics segmented by remote work arrangement |
| `AVRG FEEDBACK` | Manager feedback scores by remote work status |
| `dashboard` | Interactive visual dashboard with slicers |
| `Sheet14` / `Sheet15` | Working/staging sheets |

---

## Dataset Schema

The `ORIGINAL` sheet contains **876 rows × 21 columns**:

### Employee Identity
| Column | Type | Description |
|---|---|---|
| `Employee ID` | Integer | Unique employee identifier (e.g., `10001`) |
| `First Name` | Text | Employee first name |
| `Last Name` | Text | Employee last name |
| `Gender` | Text | Female / Male |
| `Age` | Integer | Employee age (22–64) |
| `Marital Status` | Text | Married, Single, Divorced, Widowed |

### Organisation & Role
| Column | Type | Description |
|---|---|---|
| `Department` | Text | HR, IT, Sales, Marketing, Finance, Operations |
| `Employee Type` | Text | Permanent, Contract, Intern |
| `Full-Time` | Text | Yes / No |
| `Office Location` | Text | San Francisco, Nairobi, Berlin, Tokyo, London, New York |
| `Remote Work Status` | Text | On-Site, Hybrid, Fully Remote |
| `Hire Date` | Date | Date of joining (Jan 2000 – Dec 2019) |
| `Last Promotion Year` | Integer | Year of most recent promotion |

### Compensation
| Column | Type | Description |
|---|---|---|
| `Salary` | Integer | Annual salary in USD (30,056 – 119,909) |
| `Bonus` | Float | Annual bonus amount in USD |

### Performance & Development
| Column | Type | Description |
|---|---|---|
| `Performance Score` | Integer | Score on a scale of 1–9 |
| `Manager Feedback Score` | Float | Manager-assigned feedback rating |
| `Annual Training Hours` | Integer | Training hours completed in the year |
| `Project Count` | Integer | Number of projects worked on |
| `Work Experience (Years)` | Integer | Total years of professional experience |
| `Education Level` | Text | High School, Associate's, Bachelor's, Master's, PhD |

---

## 📈 Key Statistics

| Metric | Value |
|---|---|
| Total Employees | 876 |
| Hire Date Range | Jan 2000 – Dec 2019 |
| Age Range | 22 – 64 years |
| Salary Range | USD 30,056 – USD 119,909 |
| Average Salary | USD 74,067 |
| Performance Score Range | 1 – 9 |
| Average Manager Feedback | 3.01 / 5.0 |
| Average Annual Training Hours | 103.1 hrs |
| Average Project Count | 9.5 projects |
| Work Experience Range | 1 – 39 years |

---

## Workforce Breakdown

### Departments
| Department | — |
|---|---|
| Finance | 
| HR | 
| IT | 
| Marketing | 
| Operations | 
| Sales | 

### Employee Type
| Type | Count |
|---|---|
| Intern | 297 |
| Contract | 294 |
| Permanent | 285 |

### Remote Work Status
| Status | Count |
|---|---|
| Hybrid | 303 |
| On-Site | 301 |
| Fully Remote | 272 |

### Education Level
| Level | Count |
|---|---|
| Associate's | 194 |
| Master's | 183 |
| Bachelor's | 177 |
| High School | 163 |
| PhD | 159 |

### Gender
| Gender | Count |
|---|---|
| Female | 439 |
| Male | 437 |

---

##  Analysis Modules

- **Headcount Analysis** — Employee distribution across departments
- **Salary Analysis** — Average and total salary by department; cross-tabulated by marital status
- **Performance Analysis** — Departmental performance score averages and distributions
- **Work Experience** — Average tenure and experience years by department
- **Project Involvement** — Project count spread across teams and departments
- **Bonus Analysis** — Total bonus allocation by department and employment category
- **Manager Feedback** — Feedback score benchmarks segmented by remote work arrangement
- **Remote Work Analysis** — Comparative metrics across On-Site, Hybrid, and Fully Remote employees

---

##  Office Locations

| City | Country |
|---|---|
| Nairobi | Kenya |
| Berlin | Germany |
| London | United Kingdom |
| New York | USA |
| San Francisco | USA |
| Tokyo | Japan |

---

##  Getting Started

1. Clone or download the repository
2. Open `employee_performance.xlsx` in **Microsoft Excel 2016 or later**
3. Navigate to the **`dashboard`** sheet for the interactive overview
4. Use slicers to filter by Department, Location, Employee Type, or Remote Status
5. Explore individual analysis sheets for focused breakdowns

```bash
git clone https://github.com/your-username/employee-performance-analytics.git
cd employee-performance-analytics
```

---

## Possible Use Cases

- **HR Analytics** — Understand workforce composition, compensation equity, and performance trends
- **People Operations** — Identify top-performing departments and flag training gaps
- **Compensation Benchmarking** — Compare salaries across departments, locations, and education levels
- **Remote Work Research** — Analyse productivity and feedback patterns across work arrangements
- **Excel Portfolio Project** — Demonstrates PivotTables, dashboard design, and HR domain knowledge

---

##  Notes

- Salary and bonus values are in **USD**
- Performance Score is on a **1–9 scale** (higher = better)
- Manager Feedback Score appears to be on a **1–5 scale**
- Two unnamed columns (`Unnamed: 21`, `Unnamed: 22`) exist in the raw sheet — these are likely staging artifacts and can be ignored
- Dataset covers hires from **2000 to 2019** only

---

##  Tools Used

- **Microsoft Excel** — Data organisation, PivotTables, calculated fields, and dashboard design

---

##  License

Shared for **educational and portfolio purposes**. Employee data is synthetic and does not represent real individuals.

---

##  Author

> Built and maintained by **Gloria Ngigi**  
> Feel free to fork, star, or raise an issue with suggestions!
