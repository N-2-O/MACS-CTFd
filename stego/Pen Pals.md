# Pen Pals

Open the file in Notepad++, and in the top bar go to Encoding > Convert to ANSI. There will now be lines of question marks visible. Notice that each line contains a different number of question marks and that each is 1 off from the ASCII values of the known flag format.
- first line has 78 characters (77 => M)
- second has 66 (65 => A)
- third has 68 (67 => C)
- fourth has 84 (83 => S)
- fifth has 124 (123 => {)

Write a Python script to automate the process of counting the lines and converting to ASCII:

```python
f = open("invisible_ink.txt", "r")
arr = ""
for i in f:
        arr += chr(len(i)-1)
print(arr)
f.close()
```
The flag is `MACS{learn_python_if_you_value_your_time}`
