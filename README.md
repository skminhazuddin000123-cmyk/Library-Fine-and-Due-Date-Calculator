# Library Fine and Due-Date Calculator

A small command-line Python program that calculates a library item's due date and any overdue fine from its issue date, borrowing period, return date, and per-day fine rate.

## Requirements

- Python 3
- No third-party packages are required; the program uses Python's standard library.

## Run the program

From the repository directory, run:

```bash
python Code
```

If your system uses `python3` to launch Python 3, run `python3 Code` instead.

## How to use

Enter the requested values when prompted:

1. Issue date in `DD-MM-YYYY` format.
2. Allowed borrowing period in days (an integer).
3. Fine per overdue day in rupees (a number).
4. Return date in `DD-MM-YYYY` format.

The program prints the due date and a report showing the issue date, due date, return date, overdue days, and total fine. Dates must use the specified format; invalid dates or non-numeric borrowing/fine values are not handled specially.

## Calculation

- **Due date** = issue date + allowed borrowing days
- **Overdue days** = number of days returned after the due date, with a minimum of zero
- **Total fine** = overdue days × fine per day

Returning the item on or before its due date results in no fine.

## Example

```text
===== LIBRARY FINE AND DUE-DATE CALCULATOR =====
Enter issue date (DD-MM-YYYY): 01-01-2025
Enter allowed borrowing days: 14
Enter fine per day (Rs.): 2.5
Due Date: 15-01-2025
Enter return date (DD-MM-YYYY): 18-01-2025

===== LIBRARY REPORT =====
Issue Date: 01-01-2025
Due Date: 15-01-2025
Return Date: 18-01-2025
Overdue Days: 3
Total Fine: Rs. 7.5
```
