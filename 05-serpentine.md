# serpentine.py

## Objectives

> - To be able to edit and exploit application code

1. Run 'serpentine.py'. Try to select option 'b'. Oh it didn't work, well we'll have to dive deeper into the code to get the flag.
2. Open 'serpentine.py' in a terminal editor
3. Extract the flag
<details>
<summary>Hint?</summary>
<br>
Was your first instinct to decode each individual byte in the flag and piece them together?

Well what if I told you there was an easier way! Let the program do the heavy lifting for you.

Notice in line 20 that there is a method called 'print_flag'. We just need to append it to the output when selecting option b on line 69.


</details>