# Bad Teacher

We can first login to the lecturer's account with the given credentials.

Username: `s12345` , Password: `password`

After logging in, we should be able to see the student controls panel.

![view profile form](https://github.com/Jardhyx/my-notes/blob/main/assets/Access%20Control/1.png)

There are 2 solutions to this, one using burp proxy, and the other is by using devtools.

## Recommended solution

1. Using burp proxy, we can check the parameters being sent once we click view profile.
![burp](https://github.com/Jardhyx/my-notes/blob/main/assets/Access%20Control/2.png)

2. We simply need to change the set username to Nicole Fang's username `p5678901` before forwarding the request.
![burp](https://github.com/Jardhyx/my-notes/blob/main/assets/Access%20Control/5.png)

## Alternative solution

1. Using devtools, we can locate the student controls form.
![devtools stuff](https://github.com/Jardhyx/my-notes/blob/main/assets/Access%20Control/3.png)

2. Notice the option values for each student. We can simply replace Nicholas Lim's value with Nicole Fang's by editing the HTML before clicking on "View Profile".
![devtools stuff](https://github.com/Jardhyx/my-notes/blob/main/assets/Access%20Control/4.png)