# Buffer_Overflow_Example
Code to Demonstrate Buffer Overflow Vulnerability in Simple Authentication Apps 

This Authentication App Written in C is vulnerable to Buffer Overflow Attack. This Code was Specifically Made to Demonstrate this.
This shows How Not to Do Authentication in Basic C Codes. Written as a teenage guy just starting to explore cybersecurity.

In Real Life Scenario, this kind of attack is carried out much more differently. this is just overly simplifying things.
In real life , the buffer will contain a Payload With a shellcode and when that is executed, we might get root access to the machine.
it can be used for many types of exploits including privilege escalation!




This Code Demonstrates The Buffer Overlow Vulnerability in this Authentication app.
To log in and get the "Welcome" Message, the user must type the right password 

"somestupidpassword!" - password

The Function compares the password to the supplied string(password) and authenticates the user
if the password is right.

The Exploit is in STRCPY Function. It does not map the size of the character array and hence
lets us overwrite the memory in parts that we were not supposed to write to.
Normally that would cause a Segmentation Fault, But if the Variables are arranged in a specific
order in the Stack,then it causes STRCPY to overwrite them!
