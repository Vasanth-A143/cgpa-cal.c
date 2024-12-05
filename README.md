# cgpa-cal.c
# Function to calculate CGPA
def calculate_cgpa(subjects, grades, credits):
    total_grade_points = 0
    total_credits = 0
    
    for i in range(subjects):
        total_grade_points += grades[i] * credits[i]
        total_credits += credits[i]
    
    cgpa = total_grade_points / total_credits
    return cgpa

# Input number of subjects
num_subjects = int(input("Enter the number of subjects: "))

# List to store grades and credits for each subject
grades = []
credits = []

# Input grades and credits for each subject
for i in range(num_subjects):
    grade = float(input(f"Enter grade for subject {i+1} (out of 10): "))
    credit = int(input(f"Enter credits for subject {i+1}: "))
    
    grades.append(grade)
    credits.append(credit)

# Calculate CGPA
cgpa = calculate_cgpa(num_subjects, grades, credits)

# Output the result
print(f"Your CGPA is: {cgpa:.2f}")

