#   Message Encryption-Decryption

Encryption is the process that transforms the text or information to the unrecognizable form and decryption is the process to convert the encrypted message into original form.


Message encoding and decoding is the process to first convert the original text to the random and meaningless text called ciphertext. This process is called encoding. Decoding is the process to convert that ciphertext to the original text. This process is also called the Encryption-Decryption process.
 Click on the link below to view the blog post



#   Prerequisites

 Tkinter, and base64 library.
 - Tkinter is a standard GUI python library
- base64 module provides a function to encode the binary data to ASCII characters and decode that ASCII characters back to binary data.
To install the library we use pip install command on the command prompt

```
pip install tkinter
pip install base64

```



## Project File Structure  
## Import Libraries
## Initialize Window
## Define variables
## Function to encrypt
##  Function to decode
## Decode() function has arguments – key, message
## Function to set mode


```bash

def Mode():
    if(mode.get() == 'e'):
        Result.set(Encode(private_key.get(), Text.get()))
    elif(mode.get() == 'd'):
        Result.set(Decode(private_key.get(), Text.get()))
    else:
        Result.set('Invalid Mode')

```
- If the mode set by the user is ‘e’ then the Encode() function will be called
- If the mode set to ‘d‘ then the Decode() function will be called
- Else print ‘invalid mode’
- private_key.get() and Text.get() values are pass to the arguments of Encode() and Decode() function

 

## Function to exit window
```
def Exit():
    root.destroy()

```
- root.destroy() will quit the program by stopping the mainloop()

## Function to reset window


```bash
def Reset():
    Text.set("")
    private_key.set("")
    mode.set("")
    Result.set("")         

```
This function set all variables to empty string
## Labels and Buttons
```
Label(root, font= 'arial 12 bold', text='MESSAGE').place(x= 60,y=60)
Entry(root, font = 'arial 10', textvariable = Text, bg = 'ghost white').place(x=290, y = 60)

Label(root, font = 'arial 12 bold', text ='KEY').place(x=60, y = 90)
Entry(root, font = 'arial 10', textvariable = private_key , bg ='ghost white').place(x=290, y = 90)

Label(root, font = 'arial 12 bold', text ='MODE(e-encode, d-decode)').place(x=60, y = 120)
Entry(root, font = 'arial 10', textvariable = mode , bg= 'ghost white').place(x=290, y = 120)
Entry(root, font = 'arial 10 bold', textvariable = Result, bg ='ghost white').place(x=290, y = 150)

Button(root, font = 'arial 10 bold', text = 'RESULT'  ,padx =2,bg ='LightGray' ,command = Mode).place(x=60, y = 150)

Button(root, font = 'arial 10 bold' ,text ='RESET' ,width =6, command = Reset,bg = 'LimeGreen', padx=2).place(x=80, y = 190)

Button(root, font = 'arial 10 bold',text= 'EXIT' , width = 6, command = Exit,bg = 'OrangeRed', padx=2, pady=2).place(x=180, y = 190)

root.mainloop()
```
- Label() widget use to display one or more than one line of text that users aren’t able to modify.
- Entry() widget used to create an input text field.
- Button() widget used to display button on our window
- root is the name which we refer to our window
- text which we display on the label
- font in which the text is written
- insertwidth use to set the width of the insertion cursor
- bg sets the background colour
- command is call when the button is click
- textvariable used to retrieve the current text to the entry widget
- root.mainloop() is a method that executes when we want to run our program.
##  output

basic window 

![window](https://github.com/TamanamPrudhvi/message_encryption/blob/main/Decrypt.png)

Encryption
![Encrypt](https://github.com/TamanamPrudhvi/message_encryption/blob/main/Encrypt.png)

Decryption
