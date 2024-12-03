# Bad Teacher Strikes Again

The steps to take are exactly the same as [Bad Teacher](https://github.com/Jardhyx/my-notes/blob/main/secure-coding/mimosa/Access%20Control/Bad%20Teacher.md)

However, this time we will require a manager role to be able to access Nicole Fong's profile.

## Solution

1. Using burp proxy, we can see the same parameters.

![burp](https://github.com/Jardhyx/my-notes/blob/main/assets/Access%20Control/6.png)

2. Since the require a manager role to access, we can simply add a new parameter next to it and forward the request.

![burp](https://github.com/Jardhyx/my-notes/blob/main/assets/Access%20Control/7.png)