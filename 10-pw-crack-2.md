# PW Crack 2

## Objectives

> - To be able to understand and exploit application code
> - To be able to convert from hexadecimal to ascii characters

1. Open "level2.py" in your terminal
2. Go through the code line by line, ignoring the section that has been highlighted for you to ignore. Do you notice anything _different_ this time?
<details>
<summary>Hint?</summary>
<br>
Notice on line 18 that the program runs a conditional check for the user's password. Unlike the previous challenge this is not in a human readable format. The prefix '0x' is used to denote hexadecimal bytes. Let's convert it to something readable by using this 

[online hexadecimal converter](https://gchq.github.io/CyberChef/#recipe=From_Hex('0x'))

</details>

3. Convert the password to a regular ascii string
4. Run "level2.py level2.flag.txt.enc" and enter the correct password you have found when prompted
5. Congratulations! You have found the flag. Go ahead and sumbit it!