def calculate_average(a1, a2, a3):
    total = a1 + a2 + a3
    average = total / 3
    return round(average, 2)

def get_status(avg):
    if avg >= 90 and avg <= 100:
        return "Excellent"
    elif avg >= 80 and avg <= 89:
        return "Very Good"
    elif avg >= 75 and avg <= 79:
        return "Passed"
    else:
        return "Failed"

num_students = int(input("How many students? "))

while num_students < 3:
    print("Please enter at least 3 students.")
    num_students = int(input("How many students? "))

for i in range(num_students):
    print("")
    print("--- Student", i + 1, "---")
    name = input("Enter name: ")
    act1 = float(input("Activity 1: "))
    act2 = float(input("Activity 2: "))
    act3 = float(input("Activity 3: "))

    avg_score = calculate_average(act1, act2, act3)
    status = get_status(avg_score)

    print("")
    print("Name:", name)
    print("Activity 1:", act1)
    print("Activity 2:", act2)
    print("Activity 3:", act3)
    print("Average:", avg_score)
    print("Status:", status)

print("")
print("All students processed!")
