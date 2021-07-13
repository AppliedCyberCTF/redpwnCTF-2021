# redpwnCTF-2021

* **Category:**  Crypto
* **Points:** 103pts
* **Author:** [Vivian](https://github.com/vivian-dai)

## Challenge
> I want to do an RSA!

The challenge contained `output.txt` which had these contents:
```text
n: 228430203128652625114739053365339856393
e: 65537
c: 126721104148692049427127809839057445790
```
Using [alpertron](https://www.alpertron.com.ar/ECM.HTM) we can figure out the value of phi (Euler's totient).  
Code for decripting RSA can be found [here](https://crypto.stackexchange.com/questions/19915/rsa-decryption-given-n-e-and-phin) which outputted "}43fd28ba86{galf".  
We can reverse the string for the flag
```python
print("}43fd28ba86{galf"[::-1])
```
```
FLAG: flag{68ab82df34}
```