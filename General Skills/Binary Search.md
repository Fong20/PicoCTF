# Binary Search Writeup
Summary of challenge: Understand how the binary search algorithm works by analyzing the script provided to obtain the required flag

## Step 1: Launch the Instance
We are presented with a brief introduction of the chalenge and a zip file, **challenge.zip** which would be handy later on. However, we need to start the instance to reveal more information in regards to solving the challenge. 

![Screen Shot 04-07-25 at 10 09 PM 001](https://github.com/user-attachments/assets/c360715e-c73a-4855-8966-0d60788b56b5)

## Step 2: Initiate SSH Connection

Once the instance is launched, the challenge provides us with additional information such as the ssh connection information and the password as seen below:

![Screen Shot 04-07-25 at 10 10 PM](https://github.com/user-attachments/assets/d3e74a44-6bd7-4a14-a640-c79a4d7d351f)

Paste the provided ssh information in the terminal and press enter to initiate the connection.

![Screen Shot 04-07-25 at 10 12 PM](https://github.com/user-attachments/assets/7eff039b-ab49-4d8f-8c3a-645c76d4662b)

We will be prompt to accept or reject the fingerprint for the connection. In this case, we are required to enter yes.

![Screen Shot 04-07-25 at 10 13 PM](https://github.com/user-attachments/assets/faa0a5ce-5599-4a1b-8f5f-0bcf5a934da5)

Once the fingerprint is accepted, we are required to enter the password to establish the connection. The password to be entered would be the password provided at the challenge page earlier, which is **1ad5be0d**.

![Screen Shot 04-07-25 at 10 13 PM 001](https://github.com/user-attachments/assets/e3a50d8e-798c-442b-a9ea-f0766f797816)

Once the password has been entered and successfully verified, we will be presented with the challenge itself.

![Screen Shot 04-07-25 at 10 13 PM 002](https://github.com/user-attachments/assets/c39e4455-66c1-45b0-9964-0a64cb5b124b)

## Step 3: Analyze the File
Before we could solve the challenge, we need to obtain and analyze the necessary information. As mentioned earlier, we are presented with a zip file, **challenge.zip** in the challenge page to solve the challenge. Download and unzip the zip file, and we are presented with a script named **guessing_game.sh**

![image](https://github.com/user-attachments/assets/f1a12cc6-3b44-42a3-af10-ed14ab140895)

The script shows how the binary search algorithm works which is crucial to understanding how the flag is obtained to solve the challenge.

### How the Script Works
There are 4 important variables in the script:

1. target: the targeted number to be guessed which is generated randomly between 1 and 1000
2. MAX_GUESSES: the maximum number of guesses by a player, which is 10
3. guess_count: tracks the number of guesses initiated by the player
4. guess: the value which is guessed by the player by inputting a number

Once we have understand the function of the variables, we can have a rough hunch on how the algorithm works. Below is a brief description on how the algorithm works:

1. The program will generate a random number between 1 and 1000 and store it in the target variable
2. The MAX_GUESSES variable is set to 10 so that it limits the player to only 10 attempts in guessing the correct number
3. The guess_count variable starts from 0
4. A while loop is used to loop through the player's process of guessing the number where the process will continue to be executed as long as the value of guess_count is less than MAX_GUESSES which is 10. 
5. The program prompts the user to enter a number and saving it to the guess variable. If the value of the guess variable is less than the target variable value, the program will inform the player that the value is too low. Vice versa, the program will inform the player that the value is too high
6. If the value of the guess variable is equal to the target variable value, the program will retrieve the flag from the metadata file and provide the required flag.

![Screen Shot 04-07-25 at 10 08 PM](https://github.com/user-attachments/assets/fec8a858-873a-41e0-a00a-8a35ecaefb1b)

## Step 4: Guess the Number
As we have understood how the algorithm works, it is easier for us to guess the number. Based on the script, it stated that a random number is generated between 1 and 1000 so I proceeded by guessing a number between the provided range.

- I started off with a moderate value of 500, which is to low
- I then proceeded with a higher value of 700, which is still to low
- The next value entered is 900 which is too high. This provided me a crucial information that the number is between 700 and 900.
- I then tried 800 which is still apparently too high, indicating that the number generated is between 700 and 800
- I proceeded to try 750 but the value is too low, indicating that the number generated is between 751 and 800
- I proceeded to try 770 but the value is too high, indicating that the number generated is between 751 and 769
- I proceeded to try 755 but the value is too low, indicating that the number generated is between 756 and 769
- I proceeded to try 760 but the value is still too low, indicating that the number generated is between 761 and 769
- I proceeded to try 765 but the value is still too low, indicating that the number generated is between 766 and 769
- Since I already narrowed down the range of numbers to be guessed, which is between 766 and 769, I proceeded to try the value of 766 and managed to obtain the required flag, **picoCTF{g00d_gu355_3af33d18}**

![Screen Shot 04-07-25 at 10 11 PM](https://github.com/user-attachments/assets/8c44bee8-74a1-4732-b77f-1889f0eefeda)
