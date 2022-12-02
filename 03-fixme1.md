# fixme1.py

## Objectives

> - To be able to fix issues in a python script

1. Start by downloading the required python script using the Webshell
  ```console
  wget https://artifacts.picoctf.net/c/39/fixme1.py
  ```
2. Run the python script `fixme1.py` to see what type of error is raised and take note of the line number on where the error is found
  ```console
  python3 fixme1.py
  ```
3. Fix the error in the python script by using a terminal editor
```console
vi fixme1.py
```

<details>
<summary>Hint?</summary>
<br>
You should encounter a `IndentationError` on **line 20**, to begin fixing this issue

```python
flag = str_xor(flag_enc, 'enkidu')
print('That is correct! Here\'s your flag: ' + flag)
```

</details>