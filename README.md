# Calefornia---Calendar-App

import calendar

# Prompt user to enter year and month
year = int(input("Enter year: "))
month = int(input("Enter month: "))

# Create calendar object
cal = calendar.monthcalendar(year, month)

# Print calendar header
print("{0} {1}".format(calendar.month_name[month], year))
print("Mo Tu We Th Fr Sa Su")

# Print calendar rows
for week in cal:
    row = ""
    for day in week:
        if day == 0:
            row += "   "
        else:
            row += "{0:2d} ".format(day)
    print(row)
