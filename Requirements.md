# SCHEDULING RULES

        WEEKDAYS (MONDAY - THURSDAY)
        WEEKENDS (FRIDAY - SUNDAY)

---
        Departments:

        HOST
          - 3 per day (WEEKDAYS)
          - 4 per day (WEEKENDS)
        TOGO
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
          - Generally work 5 days
          - MAXIMUM 6 days
          - Can have day & shift preferences
---

        Availability (HOSTS):

        Shifts
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

        Shifts 
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


### (EMPLOYEE)

    - Enter & Save Employee information
    - Access Employees Individually
    - Edit Employee information
    - Delete Employees
    - Mark as inactive (unspecified / within set timeline)

---

### (SCHEDULER)

    -   

---
enum class DayOfWeek 

    - Monday 
    - Tuesday 
    - Wednesday
    - Thursday 
    - Friday 
    - Saturday 
    - Sunday


enum class Department

    - Host
    - Togo

enum class ShiftPreference

    - Morning
    - EarlyMid
    - Mid
    - LateMid
    - Closer

---

## class Employee
      (Data Members):
        - HOST or TOGO variable
            - enum Department{};
        - Name variable
            - const char* Name
        - Active / Unactive status
            - bool IsActive{};
        - Container for Day objects
            - std::set<class Day> Days{};
        - Day Preference
            - enum DayPreference{};

      (Member Methods):
        - Check Available Day
            - bool IsAvailable(enum Day);
        - Function that chooses shift
            - float SelectShift(enum Day); 
        - Access day function
            - void DayMenu();
        - Set day preference
            - void SetPreference(enum DayOfWeek); 

---
## class Day

        (Data Members):
        - Name variable
            - const char* Name
        - Availability
            - bool IsAvailable;
        - Shift Preference variable
            - enum ShiftPreference{};
        - enum that represents the day
            - DayOfWeek;
        - comparison operator overload
            - bool operator<(const Day& rhs);
        - variable to check if its a weekend
            - bool IsWeekend{};

        (Member Methods):
        - Get Available Shifts
            - Shift GetShifts();
        - Get Preference
            - enum GetPreference();
        - Set Day Availablility
            - void SetDayAvailable(bool TrueFalse);
        - Set Shift Availability
            - void SetShiftAvailability();
        - Set Shift Preference
            - void SetPreference(enum ShiftPreference);


---  

## class Shift

        (Data Members):
          - Container for available shifts
              if HOST
                - std::array<std::pairs<bool, float>, 5> Shifts;
              if TOGO
                - std::array<std::pairs<bool, float>, 4> Shifts;
        
        (Member Methods):
          - Get Shift
              - std::array GetShift();
          - Set Shift
              - void SetShift();