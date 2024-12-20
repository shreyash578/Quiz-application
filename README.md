import random

def run_quiz():
    quiz = {
        "What is the capital of France?": ("A) Paris", "B) Berlin", "C) Madrid", "D) Rome", "A"),
        "Which planet is known as the Red Planet?": ("A) Earth", "B) Mars", "C) Venus", "D) Jupiter", "B"),
        "What is the smallest prime number?": ("A) 1", "B) 2", "C) 3", "D) 5", "B"),
        "Who wrote 'Hamlet'?": ("A) Charles Dickens", "B) J.K. Rowling", "C) William Shakespeare", "D) Mark Twain", "C"),
        "What is the largest mammal?": ("A) Elephant", "B) Blue Whale", "C) Great White Shark", "D) Giraffe", "B")
    }
    questions = list(quiz.keys())
    random.shuffle(questions)
    score = 0
    for question in questions:
        options = quiz[question][:-1]
        correct_answer = quiz[question][-1]
        print("\n" + question)
        for option in options:
            print(option)
        user_answer = input("Your answer (A, B, C, or D): ").strip().upper()
        if user_answer == correct_answer:
            print("Correct!")
            score += 1
        else:
            print(f"Wrong! The correct answer was {correct_answer}.")
    print(f"\nYou scored {score}/{len(quiz)}.")

if __name__ == "__main__":
    run_quiz()
