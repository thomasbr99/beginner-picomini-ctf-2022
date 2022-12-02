# picoCTF - picoGYM walkthrough: Beginner picoMini 2022

### Codebook

<details>
  <summary markdown="span"> Step one </summary>
  
  <br> Start by downloading the required files using the Webshell
  
  ```console
  wget https://artifacts.picoctf.net/c/102/code.py
  
  wget https://artifacts.picoctf.net/c/102/codebook.txt
  ```
</details>



<details>
  <summary markdown="span">Step two</summary>
  
  <br> You can use the command `ls` to check that the relevant files have been downloaded locally. Make sure that both `code.py` and `codebook.txt` are in the same directory
</details>

<details>
  <summary markdown="span">Step three</summary>
  
  <br> Executing the python file `code.py` will then print the challenge flag. 
  You can do this by entering the following command 
  ```console
  python3 code.py
  ```
</details>

### convertme.py
<details>
  <summary markdown="span">Step one</summary>
  
  <br> Start by downloading the required python script using the Webshell
  ```console
  wget https://artifacts.picoctf.net/c/31/convertme.py
  ```
</details>

<details>
  <summary markdown="span">Step two</summary>
  
  <br> Run the python script `convertme.py `
  ```console
  python3 convertme.py
  ```
</details>

<details>
  <summary markdown="span">Step three</summary>
  
  <br> You should see a randomly generated decimal value, converting this value into binary will provide the required flag. There are many websites available for converting decimal to binary, e.g. https://www.rapidtables.com/convert/number/decimal-to-binary.html
  
  ![convertme output](https://miro.medium.com/max/720/1*EVS3VMu9wXUuJNHZaFNzCg.png)
</details>

### fixme1.py
<details>
  <summary markdown="span">Step one</summary>
  
  <br> Start by downloading the required python script using the Webshell
  ```console
  wget https://artifacts.picoctf.net/c/39/fixme1.py
  ```
</details>

<details>
  <summary markdown="span">Step two</summary>
  
  <br> Run the python script `fixme1.py` to see what type of error is raised
  ```console
  python3 fixme1.py
  ```
</details>

<details>
  <summary markdown="span">Step three</summary>
  
  ![fixme1 error](https://miro.medium.com/max/720/1*USSa0Wo15jwnRS7OQmKyKQ.png)
  <br> You should encounter a `IndentationError` on **line 20**, to begin fixing this issue you will need to open the python file for edit
  ```console
  nano fixme1.py
  ```
</details>

<details>
  <summary markdown="span">Step four</summary>
  
  <br> With the python file opened, navigate to **line 20** and remove the erroneous indents. Exit `nano` by pressing CTRL and X, making sure to save your changes. Running `fixme1.py` again will now correctly print the required flag
</details>

### fixme2.py
<details>
  <summary markdown="span">Step one</summary>
  
  <br> Start by downloading the required python script using the Webshell
  ```console
  wget https://artifacts.picoctf.net/c/65/fixme2.py
  ```
</details>

<details>
  <summary markdown="span">Step two</summary>
  
  <br> Run the python script `fixme2.py` to see what type of error is raised
  ```console
  python3 fixme2.py
  ```
</details>

<details>
  <summary markdown="span">Step three</summary>
  
  ![fixme1 error](https://miro.medium.com/max/720/1*mlYHpWOlsbMF6f5OqZf2Bw.png)
  <br> You should encounter a `SyntaxError` on **line 22**, to begin fixing this issue you will need to open the python file for edit
  ```console
  nano fixme2.py
  ```
</details>

<details>
  <summary markdown="span">Step four</summary>
  
  ![fixme2 fix](https://miro.medium.com/max/720/1*czlwQZxsUc_je4-0yaPCTQ.png)
  <br> With the python file opened, navigate to **line 22** and fix the incorrect Syntax. The conditional operator `if` in Python requires two equal signs instead of one. Exit `nano` by pressing CTRL and X, making sure to save your changes. Running `fixme2.py` again will now correctly print the required flag
</details>

### Glitch Cat.py

<details>
  <summary markdown="span">Step one</summary>
  
  <br> netcat is a computer networking utility for reading from and writing to network connections using TCP or UDP. The command `nc` will allow us to connect to the the flag printing server using netcat
  ```console
  nc saturn.picoctf.net 51109
  ```
</details>

<details>
  <summary markdown="span">Step two</summary>
  
  <br> Like the challenge mentions, the service is broken. The printed flag contains ASCII characters, which are those `chr(0xXX)` values where XX is a integer number.
  To retrieve the correct format flag, we must convert these ASCII characters
  ![glitchcat ascii](https://miro.medium.com/max/720/1*ftMjXhhyhnn0BNtUfv56nw.png)
</details>

<details>
  <summary markdown="span">Step three</summary>
  
  <br> The ASCII characters can be directly converted inside the Webshell using Python. First open up Python in the webshell by entering the command `python3`. Then you may use the `print` function with the incorrected formatted flag to acquire the valid flag
  ![glitchcat print](https://miro.medium.com/max/720/1*td5MwTQg-KICaU28fAHBPw.png)
</details>

### HashingJobApp.py

<details>
  <summary markdown="span">Step one</summary>
  
  <br> netcat is a computer networking utility for reading from and writing to network connections using TCP or UDP. The command `nc` will allow us to connect to the the flag printing server using netcat
  ```console
  nc saturn.picoctf.net 57689
  ```
</details>

<details>
  <summary markdown="span">Step two</summary>
  
  ![hashingjob question](https://miro.medium.com/max/720/1*6pKJRoOfINRQ7MH5ZYrQ7A.png)
  <br> To access the flag you must `md5 hash` a randomly generated string. This can be done in web apps like the following: https://www.md5hashgenerator.com, or in your command line by using the `md5sum` tool. 
  ```console
  echo -n 'string' | md5sum
  ```
</details>

<details>
  <summary markdown="span">Step three</summary>
  
  <br> You will have to repeat the hash with two more randomly generated strings before receiving the event flag. The same method as used in step two can be repeated for the remaining conversions.
![hashing flag](https://miro.medium.com/max/720/1*svtKsmTIYGunJ4qCP-pKUw.png)
</details>
