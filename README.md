import random
min = int(input("what is the minimum number: "))
max = int(input("what is the maximum number: "))
number_question = int(input("number of question :"))
correct_answer = 0
asked_question = 0
#def average(correct_answer, number_question):
if number_question  not in range (min,max):
    print("out of range")
else:
        while  asked_question <= number_question-1:
            operator = ["+", "*"]
            print()
            print("question " + str(asked_question+1) + " out of " + str(number_question))
            number1 = random.randint(min,max)
            operator = random.choice(operator)
            number2 = random.randint(min,max)
            question = '{} {} {}'.format(number1, operator, number2)
            print(question)
            student_answer = int(input())
            if operator == "+":
                answer = number1 + number2
            else:
                answer = number1 * number2
            if answer == int(student_answer):
                print("correct")
                asked_question += 1
                correct_answer +=1
            else:
                print("incorrect")
                asked_question +=1
        print("your point is " + str(correct_answer) + " out of " + str(number_question))
 #       average (correct_answer, number_question)
        if correct_answer < int((number_question) / 2):
            print("your average is  week")
        elif correct_answer == int((number_question) / 2):
            print("your average  score is average")
        elif correct_answer == number_question:
            print("your average  score is exclent")



