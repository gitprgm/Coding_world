a = int(input("Enter first number: "))
b = int(input("Enter second number: "))

while b != 0:
    a, b = b, a % b

print("GCD =", a)


# 1. Create a gcd() function.
# 2. Use abs() for negative numbers.
# 3. Add comments.
# 4. Improve output message.

def gcd(a, b):
    while b != 0:
        a, b = b, a % b
    return abs(a)

num1 = int(input("Enter first number: "))
num2 = int(input("Enter second number: "))

print("The GCD is", gcd(num1, num2))


#Role exchange
#bug introduced: The bug occurs because a is overwritten before calculating a % b.
# 24 and 36 output should be 12 but we get 36
def gcd(a, b):
    while b != 0:
        a = b
        b = a % b
    return a

num1 = int(input("Enter first number: "))
num2 = int(input("Enter second number: "))

print("The GCD is", gcd(num1, num2))



#improved version 

def gcd(a, b):
    while b != 0:
        a, b = b, a % b
    return abs(a)

try:
    num1 = int(input("Enter first number: "))
    num2 = int(input("Enter second number: "))

    if num1 == 0 and num2 == 0:
        print("GCD is undefined.")
    else:
        print("The GCD of", num1, "and", num2, "is", gcd(num1, num2))

except ValueError:
    print("Please enter valid integers.")
