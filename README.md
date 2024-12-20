import random

def run_quiz():
    # Define the quiz questions and answers
    quiz = {
        "What is the capital of France?": ("A) Paris", "B) Berlin", "C) Madrid", "D) Rome", "A"),
        "Which planet is known as the Red Planet?": ("A) Earth", "B) Mars", "C) Venus", "D) Jupiter", "B"),
        "What is the smallest prime number?": ("A) 1", "B) 2", "C) 3", "D) 5", "B"),
        "Who wrote 'Hamlet'?": ("A) Charles Dickens", "B) J.K. Rowling", "C) William Shakespeare", "D) Mark Twain", "C"),
        "What is the largest mammal?": ("A) Elephant", "B) Blue Whale", "C) Great White Shark", "D) Giraffe", "B"),
        "What is the boiling point of water at sea level in Celsius?": ("A) 90", "B) 100", "C) 110", "D) 120", "B"),
        "Which element has the chemical symbol 'O'?": ("A) Gold", "B) Oxygen", "C) Osmium", "D) Hydrogen", "B"),
        "What is the square root of 64?": ("A) 6", "B) 7", "C) 8", "D) 9", "C"),
        "Who painted the Mona Lisa?": ("A) Vincent van Gogh", "B) Pablo Picasso", "C) Leonardo da Vinci", "D) Claude Monet", "C"),
        "What is the largest planet in our solar system?": ("A) Earth", "B) Jupiter", "C) Saturn", "D) Neptune", "B")
    }

    # Randomize the order of questions
    questions = list(quiz.keys())
    random.shuffle(questions)

    # Start the quiz
    score = 0
    for question in questions:
        options = quiz[question][:-1]  # Extract options
        correct_answer = quiz[question][-1]  # Extract correct answer

        print("\n" + question)
        for option in options:
            print(option)

        # Get user's answer
        user_answer = input("Your answer (A, B, C, or D): ").strip().upper()

        # Check if the answer is correct
        if user_answer == correct_answer:
            print("Correct!")
            score += 1
        else:
            print(f"Wrong! The correct answer was {correct_answer}.")

    # Display the final score
    print(f"\nYou scored {score}/{len(quiz)}.")

if __name__ == "__main__":
    run_quiz()
