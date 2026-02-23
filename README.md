# Lab3_Repository

# My Code

# This code will average the score, letter grade, and academic standing

# Defining the average calculating function
def calculateAverage(score1, score2, score3):
    return round((score1 + score2 + score3) / 3, 2)

# Defining what score gives you which letter grade
def getLetterGrade(avg):
    if avg >= 90:
        return "A"
    elif avg >= 80:
        return "B"
    elif avg >= 70:
        return "C"
    elif avg >= 60:
        return "D"
    else:
        return "F"

# main
def main():
    scores = []
    for i in range(1, 4):
        score = float(input(f"Enter test score {i}: "))
        while score < 0 or score > 100:
            print("Score must be 0-100!")
            score = float(input(f"Enter test score {i}: "))
        scores.append(score)

    Average = calculateAverage(scores[0], scores[1], scores[2])
    Letter = getLetterGrade(Average)
    Standing = getAcademicStanding(Letter)

    print("\nAverage Score:", Average)
    print("Letter Grade:", Letter)
    print("Academic Standing:", Standing)

if __name__ == "__main__":
    main()
