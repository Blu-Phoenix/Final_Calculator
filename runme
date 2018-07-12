"""
Program: Final_Calculator(Master).py
Developer: Michael Royer
Language: Python-3.x.x
Primum Diem: 12/2017
Modified: 03/28/2018

Description: This program is a calculator that is designed to help students know what finals they should focus on and which ones they can just glance over.

Input: The user will be asked four questions about their class. They are as follows: the total points possible, the amount of points earned, their desired percentage score, and the amount of points the are left in the class.

Output: This program in output the minimum score they have to make on their final to get their desired score.
"""


# The Input function asks the user for four different questions, and returns their answers as a float.
def Input():
    total_points = float(input("Enter the total points possible in your class.""\n"))
    your_points = float(input("Enter the amount of points that you have earned in your class up until this point.""\n"))
    desired_score = float(input("Enter the percentage score that you want to earn in the class (ex. 90, 80 or 84.5).""\n"))
    points_LOTB= float(input("Enter the amount of points possible that are left in your class.""\n"))

    return total_points, your_points, desired_score, points_LOTB


# The Calculation function the controls the processing part of the program.
def Calculation(total_points, your_points, desired_score, points_LOTB):


    # This if-statement fixes the 'divide by zero' bug.
    if points_LOTB <= 0:
        print ("Sorry mate your class is over.")
        Input()

    points_need = total_points * (desired_score / 100)
    D_score_needed = (points_need - your_points) / points_LOTB
    score_needed = D_score_needed * 100

    return score_needed, desired_score


# The Output function that controls the output part of the program.
def Output(score_needed, desired_score):

    if score_needed <= 0:
        print ("If you skip your final and still pass your class with a", desired_score, "percent.")

    if score_needed > 100:
        print ("You can't make a", desired_score, "percent in your class even if you make a perfect score on your test.")

    if (score_needed <= 100 and score_needed >= 0):
        print ("You need to make at least", score_needed, "percent on your test to make a", desired_score, "percent in your class.")


# The Main function excuites the program in order.
def Main():
    [total_points, your_points, desired_score, points_LOTB] = Input()
    [score_needed, desired_score] = Calculation(total_points, your_points, desired_score, points_LOTB)
    Output(score_needed, desired_score)


# This block excuites the program
Main()
