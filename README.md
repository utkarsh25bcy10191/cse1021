🏛️ VIT Financial Management System (CLI)

A robust, terminal-based financial ledger designed for back-office accounting operations, streamlining student fee collection and auditing.

📖 Overview

The VIT Financial Management System is a specialized Command Line Interface (CLI) tool developed to assist the accounts department in managing student finances with precision, speed, and reliability. Unlike standard, graphics-heavy student portals that can be slow and cluttered, this tool focuses entirely on the accountant's workflow.

It prioritizes high-speed data entry, rapid transaction recording during peak admission seasons, and immediate deficit tracking without the need for mouse navigation. The system utilizes a lightweight, local JSON-based database to ensure strict data persistence without the maintenance overhead of complex SQL servers, making it a highly portable and efficient solution for administrative terminals.

✨ Key Features



📊 Financial Health Dashboard

Get an instant, high-level macro-view of the institution's financial standing to aid in daily reporting and decision-making.

Real-time Deficit Tracking: Instantly visualize exactly how much revenue is outstanding across the entire student body, helping to prioritize collection efforts.

Cash Flow Analysis: Monitor total expected revenue versus total actual collected revenue, providing a clear snapshot of the institution's liquidity at any given moment.



📝 Ledger Management

Create Student Accounts: Seamlessly open new financial profiles for incoming students. The system includes automated, collision-free Registration ID generation to ensure every record is unique.

Secure Data Persistence: All records are automatically serialized and saved to school_accounts.json in real-time, ensuring that no data is lost even in the event of a sudden power failure or program exit.



💸 Transaction Recording

Multi-Mode Payments: Accurately record the nature of incoming funds by specifying payment modes (Cash, UPI, or Demand Draft), which is crucial for end-of-day reconciliation.

Official Receipt Generation: The system automatically generates and displays a detailed text-based receipt confirmation after every transaction, including timestamp, amount, mode, and remaining balance.

Overpayment Protection: Built-in validation prevents accounting errors by blocking payments that exceed the outstanding dues, ensuring the ledger never reflects a negative debt.


🔍 Audit & Compliance

Defaulter Highlighting: The audit view simplifies the identification of outstanding accounts by automatically flagging students with pending dues using visual indicators (*), allowing for rapid scanning of the debtor list.

Account Closure: Securely delete or close ledgers for students who have graduated or transferred out, ensuring the active database remains clean and relevant for current academic year operations.



🚀 Getting Started

Prerequisites

Python 3.6 or higher: Ensure Python is added to your system's PATH. You can verify this by running python --version in your terminal.

Standard Libraries Only: The system relies solely on Python's built-in libraries (json, os, random, datetime), eliminating the need for pip install or external dependencies.

Installation

Clone or Download the repository to your local machine or secure administrative drive.

Ensure the main.py script is located in a directory with write permissions, as it needs to generate and update the database file.

Usage

Open your terminal (Command Prompt on Windows, Terminal on macOS/Linux) and execute:

python main.py


Note: On first launch, the system will automatically initialize and create the school_accounts.json database file if one does not already exist.



📂 Project Structure

VIT-Accounts-System/
│
├── main.py                 # Core application logic containing the SchoolAccountant class
├── school_accounts.json    # Database (Auto-generated JSON file storing all ledgers)
└── README.md               # Comprehensive project documentation and usage guide


📸 Application Workflows

1. The Dashboard

Goal: Assess daily financial progress.
The dashboard aggregates data from all individual ledgers to provide a summary of Total Receivables (AR), Total Collected amounts, and the crucial Outstanding Deficit figure.

2. Recording a Transaction

Goal: Process a fee payment efficiently.
Select Student (via Reg ID) -> View Current Dues -> Input Payment Amount & Mode -> Generate Official Receipt.
This workflow is optimized for speed to handle long queues during fee submission days.

👨‍💻 Developer Information

Developed by: Utkarsh Agarwal

Registration ID: 25BCY10191

Department: Accounts & Backend Systems Development

⚠️ Disclaimer

This tool is intended for internal administrative use only. As it uses a local file for data storage, please ensure that the school_accounts.json file is backed up regularly (e.g., to an external drive or secure cloud folder) to prevent data loss in case of hardware failure.
