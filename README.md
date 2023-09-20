# ClinkClank

division function of  a calculator resulting in clinkclank, clink or clank depending on if it's divisible by 6, 8 or both 

# ClinkClank code

while True:
   try:
        num = int(input("Please enter a number: "))
   except ValueError:
        print("Error: The calculator can only accept whole numbers, please try again")
        continue
   def div(num):
    if num % 6 == 0 and num % 8 == 0:
        return "clinkclank"
    elif num % 6 == 0:
        return "clink"
    elif num % 8 == 0:
        return "clank"
    else:
        return num

   result1 = div(num)
   print(result1)

   '''test of the clinkclank/clink/clank for div(num) function'''

   try: assert div(num) == "clinkclank", f"Did not get clinkclank for div {num}"
   except AssertionError as error: print(f"Fail:{error}")

   try: assert div(num) == "clink", f"Did not get clink for div {num}"
   except AssertionError as error: print(f"Fail {error}")
   try: assert div(num) == "clank", f"Did not get clank for div {num}"
   except AssertionError as error: print(f"Fail {error}")

   try: assert div(num) == "Error: The function can only accept whole numbers", "Did not get error message when dividing floats"
   except AssertionError as error: print(f"Fail {error}") 
    
   print ("all tests have been run")

   '''We can infer from the div(num) that the div() is working properly since it gives error message on the float test. We were able to make sure on the float and "string" test'''
