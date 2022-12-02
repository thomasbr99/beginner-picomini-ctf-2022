# fixme2.py

## Objectives

> - To be able to fix issues in a python script

1. Start by downloading the required python script using the Webshell
  ```console
  wget https://artifacts.picoctf.net/c/65/fixme2.py
  ```
2. Run the python script `fixme2.py` to see what type of error is raised and take note of the line number on where the error is found
  ```console
  python3 fixme2.py
  ```
3. Fix the error in the python script by using a terminal editor
```console
vi fixme1.py
```

<details>
<summary>Hint?</summary>
<br>
With the python file opened, navigate to **line 22** and fix the incorrect Syntax. The conditional operator `if` in Python requires two equal signs instead of one.

```python
if flag == "":
print('String XOR encountered a problem, quitting.')
```

</details>