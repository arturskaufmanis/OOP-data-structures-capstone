# Object-oriented-programming-capstone
A comprehensive, object-oriented inventory management system built with Python, designed for retail businesses to efficiently manage shoe inventory with advanced analytics, reporting, and business intelligence features.


## 👟 Shoe Inventory Management System

A Python-based inventory management application that demonstrates Object-Oriented Programming concepts, data structure manipulation, and file handling. This capstone project implements a practical business solution with inventory tracking, analytics reporting, and data persistence capabilities.

## 🎯 Project Overview

This shoe inventory management system provides functionality for retail inventory tracking and basic business analytics. The application features object-oriented design, file-based data storage, and a command-line interface for managing shoe inventory with features like stock monitoring, search capabilities, and automated reporting.

## ✨ Key Features

### 🏗️ Object-Oriented Design
- **Class-Based Architecture** - Implementation using Shoe and InventoryManager classes
- **Custom Exception Handling** - ShoeError class for inventory-specific error management
- **Data Encapsulation** - Proper use of private methods and controlled data access
- **Method Organization** - Logical grouping of functionality within classes

### 📊 Inventory Operations
- **Stock Management** - Add, view, and update shoe inventory items
- **Search Functionality** - Find shoes by product code
- **Restocking System** - Identify and restock low-quantity items
- **Data Validation** - Input validation for costs, quantities, and product codes

### 📈 Reporting & Analytics
- **Inventory Valuation** - Calculate total value of inventory items
- **Stock Analysis** - Identify highest quantity items for sales opportunities
- **Formatted Display** - Professional table formatting using tabulate library
- **Basic Visualization** - Simple ASCII charts for data representation

### 💾 Data Management
- **File Persistence** - CSV-based data storage for tasks and user information
- **Backup System** - Automatic backup creation before data modifications
- **Error Handling** - Graceful handling of file operations and data corruption
- **Logging** - Basic logging system for tracking operations and errors

## 🛠️ Technologies & Concepts Demonstrated

### Core Python Skills
- **Object-Oriented Programming** - Classes, objects, inheritance, and encapsulation
- **Data Structures** - Lists, dictionaries, and data manipulation
- **File I/O Operations** - Reading from and writing to CSV files
- **Exception Handling** - Try/catch blocks and custom exception classes
- **String Processing** - Data parsing, formatting, and validation

### Libraries Used
- **pandas** - Data manipulation and analysis operations
- **tabulate** - Professional table formatting for console output
- **logging** - System logging and error tracking
- **os/sys** - File system operations and program control

## 🚀 Installation & Setup

### Prerequisites
- **Python 3.6+** - Required for type hints and modern Python features
- **Required Libraries**:
  ```bash
  pip install pandas tabulate
  ```

### Setup Instructions
```bash
# Download the project files
git clone <repository-url>
cd OOP-Data-Structures-Capstone

# Run the application
python inventory.py
```

### File Structure
```
OOP-Data-Structures-Capstone/
├── README.md
├── inventory.py              # Main application file
├── inventory.txt             # Data storage file (created automatically)
├── inventory_backup.txt      # Backup file (created automatically)
└── inventory_system.log      # Log file (created automatically)
```

## 📖 Usage Guide

### Starting the Application
```bash
python inventory.py
```

### Menu Options

| Option | Description | Functionality |
|--------|-------------|---------------|
| 1 | Read Shoes Data from File | Load existing inventory data |
| 2 | Add New Shoe | Create new inventory entries |
| 3 | View All Shoes | Display complete inventory list |
| 4 | Re-stock Shoes | Find and restock low-quantity items |
| 5 | Search for a Shoe | Search inventory by product code |
| 6 | Calculate Value Per Item | Display inventory values |
| 7 | Find Highest Quantity Shoe | Identify overstocked items |
| 8 | Exit | Save and close application |

### Basic Operations

**Adding New Inventory:**
```
=== Add New Shoe ===
Enter the country: South Africa
Enter the code: SKU001
Enter the product name: Running Shoes
Enter the cost (numeric value): 89.99
Enter the quantity (whole number): 25
```

**Viewing Inventory:**
```
=== Shoe Inventory ===
┌─────────────────┬─────────┬───────────────┬─────────┬──────────┬─────────┐
│ Country         │ Code    │ Product       │ Cost    │ Quantity │ Value   │
├─────────────────┼─────────┼───────────────┼─────────┼──────────┼─────────┤
│ South Africa    │ SKU001  │ Running Shoes │ $89.99  │ 25       │ $2249.75│
└─────────────────┴─────────┴───────────────┴─────────┴──────────┴─────────┘
```

## 🏗️ Code Architecture

### Class Structure
```python
class Shoe:
    """Represents individual shoe inventory items"""
    def __init__(self, country, code, product, cost, quantity)
    def get_cost(self) -> float
    def get_quantity(self) -> int
    def update_quantity(self, new_quantity: int)
    def to_dict(self) -> dict

class InventoryManager:
    """Handles inventory operations and file management"""
    def read_shoes_data(self) -> bool
    def save_shoes_data(self) -> bool
    def capture_shoes(self) -> bool
    def view_all(self) -> None
    def re_stock(self) -> bool
    def search_shoe(self) -> list
    def value_per_item(self) -> None
    def highest_qty(self) -> Shoe

class ShoeError(Exception):
    """Custom exception for inventory-related errors"""
```

### Supporting Functions
```python
def get_valid_choice(min_val: int, max_val: int) -> int
def display_menu() -> None
def main() -> None
```

## 🎓 Programming Concepts Applied

### Object-Oriented Programming
- **Class Design** - Creating classes to represent real-world entities (Shoe, InventoryManager)
- **Encapsulation** - Hiding internal data and providing controlled access through methods
- **Inheritance** - Custom exception class inheriting from base Exception class
- **Abstraction** - Simplifying complex operations through well-defined interfaces

### Data Structures & Algorithms
- **List Operations** - Filtering, sorting, and searching through inventory data
- **Dictionary Usage** - Converting objects to dictionaries for data processing
- **Data Validation** - Ensuring data integrity through input validation
- **File Processing** - Parsing CSV data and handling file operations

### Error Handling & Validation
- **Custom Exceptions** - Creating domain-specific error types
- **Input Validation** - Checking user input for correct types and ranges
- **File Error Handling** - Managing file not found, permission, and corruption issues
- **Graceful Degradation** - Providing fallback options when errors occur

## 📈 Technical Features

### Data Management
- **CSV File Operations** - Reading and writing structured data
- **Automatic Backups** - Creating backups before modifying data
- **Data Integrity** - Validating data consistency and format
- **Transaction Logging** - Recording operations for debugging and auditing

### User Interface
- **Menu-Driven Interface** - Clear navigation and option selection
- **Formatted Output** - Professional table display using tabulate
- **Input Validation** - User-friendly error messages and retry options
- **Visual Feedback** - Clear success and error notifications

### Business Logic
- **Inventory Calculations** - Computing values, totals, and statistics
- **Stock Management** - Identifying low stock and restocking needs
- **Search Operations** - Finding specific items by various criteria
- **Reporting** - Generating useful business insights from data

## 🔧 Technical Specifications

### System Requirements
- **Python Version** - 3.6 or higher
- **Dependencies** - pandas, tabulate (installable via pip)
- **Storage** - Text file storage for data persistence
- **Platform** - Cross-platform (Windows, macOS, Linux)

### Performance Considerations
- **Memory Usage** - Loads all data into memory for fast operations
- **File I/O** - Efficient reading and writing of CSV data
- **Error Recovery** - Handles common file system issues
- **Scalability** - Suitable for small to medium inventory sizes

## 🎯 Learning Outcomes

This project demonstrates understanding of:

- **OOP Principles** - Practical application of classes, objects, and inheritance
- **Data Management** - File operations, data validation, and persistence
- **User Interface Design** - Creating intuitive command-line interfaces
- **Error Handling** - Comprehensive exception management and user feedback
- **Code Organization** - Modular design and separation of concerns
- **Problem Solving** - Translating business requirements into working code

## 🚀 Potential Improvements

Areas for future development:

- **Database Integration** - Replace file storage with SQLite database
- **Web Interface** - Create a web-based version using Flask
- **Data Visualization** - Add charts and graphs for better analytics
- **User Management** - Add user accounts and permissions
- **Advanced Search** - Implement more complex search filters
- **Export Features** - Add PDF and Excel export capabilities

## 📝 Development Notes

This project follows standard Python conventions:

- **PEP 8 Style Guide** - Consistent code formatting and naming
- **Type Hints** - Function and method parameter/return type annotations
- **Documentation** - Comprehensive docstrings for all classes and methods
- **Error Handling** - Proper exception handling throughout the application
- **Code Comments** - Clear explanations for complex logic sections

## 📄 Project Purpose

This project was created as a capstone demonstration of Object-Oriented Programming concepts, data structure manipulation, and practical software development skills using Python.
