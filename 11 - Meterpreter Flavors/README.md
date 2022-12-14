# Meterpreter Flavors

- As discussed, Metasploit payloads can be initially divided into two categories; `inline` (also called **single**) and `staged`.

- Also, `staged` payloads are sent to the target in `two` steps. 

- An initial part is installed (the `stager`) and requests the rest of the payload. This allows for a smaller initial payload size. 

- The `inline(single)` payloads are sent in a single step. 

- Meterpreter payloads are also divided into `stagged` and `inline` versions. However, Meterpreter has a wide range of different versions you can choose from based on your target system. 

- The easiest way to have an idea about available Meterpreter versions could be ***to list them*** using **[msfvenom](https://github.com/ShubhamJagtap2000/Metasploit/tree/main/09%20-%20msfvenom)**, as seen below. 

  ![image](https://user-images.githubusercontent.com/63872951/187142753-1904d39f-d8a6-40a4-a176-beedab28aef9.png)
  
- We have used the `msfvenom --list payloads` command and grepped "meterpreter" payloads (adding `| grep meterpreter` to the command line), so the output only shows these. 

- You can try this command on the AttackBox provided in [this room](https://tryhackme.com/room/meterpreter).


- The list will show Meterpreter versions available for the following platforms;

   - Android
   - Apple iOS
   - Java
   - Linux
   - OSX
   - PHP
   - Python
   - Windows

- Your decision on which version of Meterpreter to use will be mostly based on three factors;

   - **Factor 1:** The target operating system (Is the target operating system Linux or Windows? Is it a Mac device? Is it an Android phone? etc.)
   - **Factor 2:** Components available on the target system (Is Python installed? Is this a PHP website? etc.)
   - **Factor 3:** Network connection types you can have with the target system (Do they allow raw TCP connections? Can you only have an HTTPS reverse connection? Are IPv6 addresses not as closely monitored as IPv4 addresses? etc.) 

- If you are `not` using Meterpreter as ***a standalone payload*** generated by `Msfvenom`, your choice may also be ***limited*** by the exploit. 

- You will notice some exploits will have a default Meterpreter payload, as you can see in the example below with the `ms17_010_eternalblue` exploit. 

    ![image](https://user-images.githubusercontent.com/63872951/187143494-8351eee2-d0cb-413e-a120-7b77023ab931.png)

-  You can also list other available payloads using the show `payloads command` with any module. 

    ![image](https://user-images.githubusercontent.com/63872951/187143567-d7cc360a-6545-49f0-a71d-d77854d30616.png)

















