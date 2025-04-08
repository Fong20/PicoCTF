# Binary Search Writeup
Summary of challenge: Understand how the binary search algorithm works through the script provided to obtain the required flag

## Step 1: Launch the instance
We are presented with a brief introduction of the chalenge and a zip file. However, we need to start the instance to reveal more information in regards to solving the challenge. 

![Screen Shot 04-07-25 at 10 09 PM 001](https://github.com/user-attachments/assets/c360715e-c73a-4855-8966-0d60788b56b5)

## Step 2: Initiate SSH Connection

- Once the instance is launched, the challenge provides us with additional information such as the ssh connection information and the password as seen below:

![Screen Shot 04-07-25 at 10 10 PM](https://github.com/user-attachments/assets/d3e74a44-6bd7-4a14-a640-c79a4d7d351f)

- Paste the provided ssh information in the terminal and press enter to initiate the connection.

![Screen Shot 04-07-25 at 10 12 PM](https://github.com/user-attachments/assets/7eff039b-ab49-4d8f-8c3a-645c76d4662b)

- We will be prompt to accept or reject the fingerprint for the connection. In this case, we are required to enter yes.

![Screen Shot 04-07-25 at 10 13 PM](https://github.com/user-attachments/assets/faa0a5ce-5599-4a1b-8f5f-0bcf5a934da5)

- Once the fingerprint is accepted, we are required to enter the password to establish the connection. The password to be entered would be the password provided at the challenge page earlier, which is **1ad5be0d**.

![Screen Shot 04-07-25 at 10 13 PM 001](https://github.com/user-attachments/assets/e3a50d8e-798c-442b-a9ea-f0766f797816)

- Once the password has been entered and successfully verified, we will be presented with the challenge itself.

![Screen Shot 04-07-25 at 10 13 PM 002](https://github.com/user-attachments/assets/c39e4455-66c1-45b0-9964-0a64cb5b124b)

## Step 3: Analyze the file
As mentioned earlier, we are presented with a zip file, **challenge.zip** in the challenge page to solve the challenge. 

Download the zip file and unzip the file, we are presented with a script named **guessing_game.sh**

![image](https://github.com/user-attachments/assets/f1a12cc6-3b44-42a3-af10-ed14ab140895)

The script shows how the binary search algorithm works which is crucial to understanding how the flag is obtained to solve the challenge.

There are 4 important variables which are as mentioned below:
- target: the targeted number to be guessed which is generated randomly between 1 and 1000
- MAX_GUESSES: the maximum number of guesses by a player, which is 10
- guess_count: tracks the number of guesses initiated by the player
- guess: the value which is guessed by the player by inputting a number

![Screen Shot 04-07-25 at 10 08 PM](https://github.com/user-attachments/assets/fec8a858-873a-41e0-a00a-8a35ecaefb1b)

