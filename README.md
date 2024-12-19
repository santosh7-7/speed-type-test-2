import time
import random

def generate_r_t():
    sentences = [
        "Amrita Vishwa Vidyapeetham.",
        "Dr.v.Thanammal Indu.",
        "java is most troublesome programming language",
        "why fear when indu mam is here !",
        "We are about to learn Front End Devolopment in our second semester"
    ]
    return random.choice(sentences)

def typing_test():
    print("Welcome to the Speed Typing Test!")
    print("You will be given a sentence to type. Type it as quickly and accurately as possible.")
    r_t = generate_r_t()
    print("\nYour sentence is:")
    print(r_t)
    input("\nPress Enter when you are ready to start typing...")
    s_t = time.time()
    user_input = input("\nType the sentence here: ")
    end_time = time.time()
    elapsed_time = end_time - s_t
    if user_input.strip() == r_t:
        print("\nCongratulations! You typed the sentence correctly.")
    else:
        print("\nOops! There were errors in your typing.")
    print(f"Time taken: {elapsed_time:.2f} seconds")

def main():
    while True:
        typing_test()
        play_again = input("\nDo you want to try again? (yes/no): ").strip().lower()
        if play_again != 'yes':
            print("\nThank you for playing! Goodbye!")
            break

if __name__ == "__main__":
    main()
