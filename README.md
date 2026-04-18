def get_grades(marks):
    if marks>= 90:
        return 'A', "Excellent! Outstanding work!🎊👏👏"
    elif marks>=75:
        return "B", "Very good! Keep it up!Let's aim for higher👍👍"
    elif marks>=50:
        return "C","Good effort! Keep improving!"
    elif marks>= 35:
         return "D", "You passed! Don't give up!"
    else:
          return "F", "Don't worry, try again! ❤️"

#input student name
name = input("Enter student name:")

#Validate marks input

while True:
    try:
        marks= float(input("Enter marks (0-100):"))
        
        if marks < 0 or marks > 100:
            print("Marks must be between 0 and 100")
            continue

        break

    except ValueError:
        print("Please enter a valid number")
    
#Get grade messgae

grade,message=get_grades(marks)

#output
print("\n📊 RESULT FOR", name.upper() + ":")
print("Marks:", int(marks), "/100")
print("Grade:", grade)
print("Message:", message)
