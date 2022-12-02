# Glitch Cat

## Objectives

> - To be able to use networking tool netcat
> - To be able to convert hex characters to ascii

1. netcat is a computer networking utility for reading from and writing to network connections using TCP or UDP. The command `nc` will allow us to connect to the the flag printing server using netcat
  ```console
  nc saturn.picoctf.net 51109
  ```
2. Like the challenge mentions, the service is broken. The printed flag contains ASCII characters, which are those `chr(0xXX)` values where XX is a integer number.
  To retrieve the correct format flag, we must convert these ASCII characters
  ![glitchcat ascii](https://miro.medium.com/max/720/1*ftMjXhhyhnn0BNtUfv56nw.png)
3. The ASCII characters can be directly converted inside the Webshell using Python.

<details>
<summary>Hint?</summary>
<br>

First open up Python in the webshell by entering the command `python3`. Then you may use the `print` function with the incorrected formatted flag to acquire the valid flag
  ![glitchcat print](https://miro.medium.com/max/720/1*td5MwTQg-KICaU28fAHBPw.png)

</details>

