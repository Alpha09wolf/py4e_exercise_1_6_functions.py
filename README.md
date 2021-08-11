# py4e_exercise_1_6_functions.py
# pay computation
def computepay():
    while True:
        hours = input("Enter hours: ")
        if hours == 'done':
            print("All done!")
            quit()
        try:
            f_hours = float(hours)
        except ValueError:
            print("Error, please enter numeric input")
            continue
        rate = input("Enter rate: ")
        try:
            f_rate = float(rate)
        except ValueError:
            print("Error, please enter numeric input:\nrestarting...")
            continue
        if f_hours > 40:
            extra_hours = ((f_hours - 40) * 1.5) + 40
            extra_pay = extra_hours * f_rate
            print("Pay: ", extra_pay)
        else:
            pay = float(hours) * float(rate)
            print("Pay:", pay)


# temp converter
def computeconvert():
    while True:
        celcius = input("Enter degrees in celcius: ")
        if celcius == 'done':
            print("All done!")
            quit()
        try:
            f_celcius = float(celcius)
        except ValueError:
            print("Invalid input: please enter numeric input.")
            continue
        f_formula_conversion = (f_celcius * 9 / 5) * 1.5 + 32
        print("Farenheit: ", round(f_formula_conversion))


# grader
def computegrade():
    while True:
        score = input("Enter score: ")
        if score == 'done':
            print("All done!")
            quit()
        try:
            f_score = float(score)
        except ValueError:
            print("Bad score")
            continue
        while 0.0 < f_score < 1.0:
            if f_score >= 0.9:
                print("A")
                break
            if f_score >= 0.8:
                print("B")
                break
            if f_score >= 0.7:
                print("C")
                break
            if f_score >= 0.6:
                print("D")
                break
            if f_score < 0.6:
                print("F")
                break
        else:
            print("Bad score")


# counter
def computecounter():
    count = 0
    tot = 0.0
    while True:
        u_num = input("Enter a number: ")
        if u_num == 'done':
            break
        try:
            fu_num = float(u_num)
        except ValueError:
            print("Invalid input")
            continue
        count = count + 1
        tot = tot + fu_num
    print(tot, count, tot / count)


# Max_min calculator
def computemaxmin():
    biggest = 0.0
    smallest = 999999999999999999999999999999999999999999999999999.99
    while True:
        prompt = input("Enter a number: ")
        if prompt == 'done':
            break
        try:
            f_prompt = float(prompt)
        except ValueError:
            print("Invalid input")
            continue
        if f_prompt >= float(biggest) or None:
            biggest = prompt
        if f_prompt <= float(smallest):
            smallest = prompt
    print("Maximum:", biggest, "\nMinimum", smallest)
