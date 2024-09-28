```mermaid
flowchart TD
A[Generate random number $Value] --> B{Is number between 1-20?}
B --> |Yes| C[Continue]
B --> |No| D[Regenerate Number]
D --> A
C --> E[Present User Input Dialogue Box for Guess]
E --> F{Verify user $input is numeric number between 1-20}
F --> |Pass| G{Compare $input to $Value}
G --> |$Value > $input| H[Present 'Guess too low' feedback to user]
G --> |$Value < $input| I[Present 'Guess too high' feedback to user]
G --> |$Value = $input| J[Present **'You Got It!'** feedback to user]
H --> E
I --> E
F --> |Fail| K[Present 'Invalid Input' feedback to user]
K --> E
```

1. Computer generates a random number, set this number as $Value
2. Run a check to verify generated number is a numeric value between 1-20
    1. If yes, continue
    2. If no, return to step 1
3. Present user with input dialogue box and instructions to enter a number between 1-20 to guess $Value, set user input as $input
4. Verify $input is numeric value between 1-20
    1. If Fail, return to step 3
    2. If Pass, continue to step 5
5. Compare $input to $Value
    1. If $Value>$input, present "Guess too low" to user
        1. Return to step 3
    2. If $Value<$input, present "Guess too high" to user
        1. Return to step 3
    3. If $Value=$input, present **"You Got It"** to user