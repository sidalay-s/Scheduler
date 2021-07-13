# (WEEKLY SCHEDULING)

WEEKDAYS (MONDAY - THURSDAY)

WEEKENDS (FRIDAY - SUNDAY)

Departments:

- Hosts
  - 3 per day (WEEKDAYS)
  - 4 per day (WEEKENDS)
- To-go Specialists
  - 3 per day (WEEKDAYS)
  - 4 per day (WEEKENDS)

Shift Times:
- Shifts are 8 hours not including 30 min break
- Ideally 7 hours not including 30 min break

30 minute break:
- Has to be before 5 hours of work
- Only one person per department on break at a time
    - Host & To-go Specialist can be on break together
    - Host & Host || To-go & To-go CAN NOT be on break together

Employees:
- Work 5 days
- Exceptions (MAXIMUM 6 days)

Availability (HOSTS):

- Shift 
  - Morning "Opening Shift" 
    - (10:30)
  - Early mid (WEEKENDS ONLY) 
    - (11:30)
  - Mid 
    - (12:30)
  - Late mid (WEEKENDS ONLY)
    - (3:00)
  - Dinner "Closer" 
    - (4:00 || 5:00 || 6:00)

Availability (TOGO SPECIALISTS):

- Shift 
  - Morning "Opening Shift" 
    - (10:15)
  - Early mid (WEEKENDS ONLY) 
    - (N/A)
  - Mid 
    - (12:00)
  - Late mid (WEEKENDS ONLY) 
    - (3:00)
  - Dinner "Closer" 
    - (5:30 || 6:00)



# PROGRAM


(EMPLOYEE)

- Enter & Save Employee information
- Access Employees Individually
- Edit Emloyee information
- Delete Employees
- Mark as inactive (unspecified / within set timeline)

---

- Generate schedule
- 

---
enum class DayOfWeek {
    Monday, Tuesday, 
    Wednesday, Thursday, 
    Friday, Saturday, Sunday
}

### class Day

- Data Members:
  - std::string_view Name;
  - DayOfWeek {};

### class Employee
- Data members:
  - std::string_view Name;
  - bool IsActive{};
  - std::set<class Day> Days{}