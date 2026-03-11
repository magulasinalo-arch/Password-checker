password = input("Enter your password: ")

# Basic checks
length = len(password)
has_number = any(char.isdigit() for char in password)
has_upper = any(char.isupper() for char in password)
has_lower = any(char.islower() for char in password)
has_symbol = any(not char.isalnum() for char in password)

# Score
score = sum([length>=8, has_number, has_upper, has_lower, has_symbol])

if score == 5:
    print("Strong password ✅")
elif 3 <= score < 5:
    print("Medium password ⚠️")
else:
    print("Weak password ❌")