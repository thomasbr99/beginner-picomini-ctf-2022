# HashingJobApp

## Objectives

> - To be able to use networking tool netcat
> - To be able to carry out md5 hashing

1. netcat is a computer networking utility for reading from and writing to network connections using TCP or UDP. The command `nc` will allow us to connect to the the flag printing server using netcat
  ```console
  nc saturn.picoctf.net 57689
  ```
2. Using md5, hash the quote and provide it as an answer
3. Repeat this for the next 2 quotes too

<details>
<summary>Hint?</summary>
<br>

 ![hashingjob question](https://miro.medium.com/max/720/1*6pKJRoOfINRQ7MH5ZYrQ7A.png)
  <br> To access the flag you must `md5 hash` a randomly generated string. This can be done in web apps like the following: https://www.md5hashgenerator.com, or in your command line by using the `md5sum` tool. 
  ```console
  echo -n 'string' | md5sum
  ```

</details>