# PW Crack 5

This time our list of passwords have gotten much longer and are now placed in a completely separate file called 'dictionary.txt'. How will we brute force it this time around?

## Objectives

> - To be able to understand and exploit application code
> - To be able to conceptualise brute force attacks
> - To be able to create short scripts to carry out brute force attacks

1. Edit 'leve5.py' file to open the 'dictionary.txt'
2. Use a for loop to iterate through the potential passwords in the dictionary
<details>
<summary>Hint?</summary>
<br>
Try using pythons inbuilt function called open() to read the file. Its default behaviour is to read through the file line by line which is convenient for us since this is how the passwords are separated in 'dictionary.txt'.

>Still stuck? Remember that there are invisible characters you have to be wary of. These are whitespace characters like ' \t\r\n' which affects the hashing of the string. You need to trim these before hashing.

</details>
