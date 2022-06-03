# rock_paper_scissors
# A simple Rock, Paper Scissors game using Python 3

    import random 

    choice_list = ["R", "S", "P"]
    prompt = "Pick an option: Rock (R), Paper (P), Scissors (S). R, P or S? "

    entry = None

    player_output = entry

    CPU_choice = random.choice(choice_list)

    while True:
    # To convert player and CPU input from R, P, S to Rock, Paper, Scissors, to be outputted on screen
    
        entry = input(prompt)
        if entry == "R":
            player_output = "Rock"
    
        if entry == "S":
            player_output = "Scissors"
    
        if entry == "P":
            player_output = "Paper"

        if CPU_choice == "R":
            output = "Rock"
    
        if CPU_choice == "S":
            output = "Scissors"
    
        if CPU_choice == "P":
            output = "Paper"  
    

        choice_notif = f"Player ({player_output}) : CPU ({output})"

        if entry not in choice_list:
            print("invalid choice. Try type R, P or S")
        elif entry == CPU_choice:
            print(choice_notif)
            print("That's a tie. Try again.")
    
        elif entry == "R" and CPU_choice == "S":
            print(choice_notif)
            print("You win! Congratulations!")
            break

        elif entry == "S" and CPU_choice == "P":
            print(choice_notif)
            print("You win! Congratulations!")
            break

        elif entry == "P" and CPU_choice == "R":
            print(choice_notif)
            print("You win! Congratulations!")
            break
    
        else:
            print(choice_notif)
            print("You lose.")
            break
