print("="*50)
print("      PERSONAL POCKET CGPA CALCULATOR")
print("="*50)

num_courses = int(input("Enter number of courses: "))

total_units = 0
total_points = 0

for i in range(num_courses):

    print("\nCourse", i + 1)

    course = input("Course Code: ")
    unit = int(input("Course Unit: "))
    score = float(input("Score: "))

    # Grade determination using selection statements
    if score >= 70:
        grade = "A"
        point = 5

    elif score >= 60:
        grade = "B"
        point = 4

    elif score >= 50:
        grade = "C"
        point = 3

    elif score >= 45:
        grade = "D"
        point = 2

    elif score >= 40:
        grade = "E"
        point = 1

    else:
        grade = "F"
        point = 0

    quality_point = point * unit

    total_units += unit
    total_points += quality_point

    print("-----------------------------")
    print("Course:", course)
    print("Grade :", grade)
    print("Grade Point:", point)
    print("Quality Point:", quality_point)

cgpa = total_points / total_units

print("\n")
print("="*50)
print("RESULT")
print("="*50)
print("Total Credit Units :", total_units)
print("Total Quality Points:", total_points)
print("CGPA:", round(cgpa,2))

# Classification

if cgpa >= 4.50:
    classification = "First Class"

elif cgpa >= 3.50:
    classification = "Second Class Upper"

elif cgpa >= 2.40:
    classification = "Second Class Lower"

elif cgpa >= 1.50:
    classification = "Third Class"

elif cgpa >= 1.00:
    classification = "Pass"

else:
    classification = "Fail"

print("Classification:", classification)

print("="*50)
