# 📅 Date Library for C++

## Overview 🎯

The **clsDate** library is a powerful C++ class designed to simplify date manipulation and operations. It provides comprehensive functionality for working with dates, including validation, date arithmetic, date formatting, and system date retrieval.

## Features ✨

- **Multiple Constructors**: Flexible initialization methods
  - Default constructor (current system date)
  - Constructor from formatted string
  - Constructor from individual day, month, year components
  - Constructor from day order in year

- **Date Properties**: Easy access and modification
  - Get/Set Day
  - Get/Set Month
  - Get/Set Year
  - Property-based access for intuitive usage

- **Date Operations** 🔄
  - Validate dates for correctness
  - Get system date automatically
  - Convert dates to string format
  - Calculate day order in year
  - Determine leap years
  - Calculate number of days in a month

- **Date Arithmetic**
  - Add/subtract days from dates
  - Calculate age
  - Compare dates
  - Calculate difference between dates

- **Display Methods**
  - Print dates in formatted manner
  - String conversion

## Installation 📦

1. **Download the clsDate library** from this repository
2. **Download the clsString library** from its separate repository and place it in the same directory
3. Include both header files in your project:

```cpp
#include "clsDate.h"
#include "clsString.h"
```

> **Note**: The `clsDate` library depends on `clsString` for string manipulation operations. Make sure both header files are in the same directory for the library to work without issues.

## Usage Example 💡

```cpp
#include <iostream>
#include "clsDate.h"

using namespace std;

int main() {
    // Create a date from current system date
    clsDate Today;
    Today.Print();
    
    // Create a date from individual components
    clsDate BirthDate(15, 6, 1990);
    cout << BirthDate.Day << "/" << BirthDate.Month << "/" << BirthDate.Year << endl;
    
    // Create a date from string format
    clsDate SpecificDate("25/12/2025");
    
    // Validate a date
    if (BirthDate.IsValid()) {
        cout << "Valid date!" << endl;
    }
    
    // Get system date
    clsDate SystemDate = clsDate::GetSystemDate();
    
    return 0;
}
```

## Class Structure 🏗️

### Main Methods:

| Method | Description |
|--------|-------------|
| `clsDate()` | Default constructor - initializes with current system date |
| `clsDate(string sDate)` | Constructor from formatted string (DD/MM/YYYY) |
| `clsDate(short Day, short Month, short Year)` | Constructor from individual components |
| `IsValid()` | Validates the current date |
| `IsValidDate(clsDate Date)` | Static method to validate a given date |
| `GetSystemDate()` | Returns the current system date |
| `Print()` | Displays the date in formatted output |
| `DateToString()` | Converts date to string format |

## Requirements 📋

- C++ compiler (C++11 or later)
- **clsString** library (must be downloaded separately and placed in the same directory)
- Standard C++ libraries (`<iostream>`, `<string>`, `<ctime>`)

## Dependencies 🔗

This library requires:
- **clsString Library**: A companion string manipulation library that handles string splitting and parsing operations

Both libraries must be kept in the same directory for proper functionality.

## Future Updates 🚀

This library is actively maintained with planned enhancements:
- Additional date formatting options
- More sophisticated date arithmetic operations
- Localization support for different date formats
- Performance optimizations
- Enhanced error handling

We are committed to continuously improving this library based on community feedback.

## Author 👨‍💻

**Ali Talal Ibrahem**

**Date**: May 1, 2026

---

*This library is provided as-is for educational and practical use in C++ projects involving date operations.*