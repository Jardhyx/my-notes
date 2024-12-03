# Syndica

We know that syndica has web filtering to prevent the word "alert" from being searched. That means we must encrypt the word "alert" in our solution. Typing anything into the search query will cause the URL to be updated.

![mafia](https://github.com/Jardhyx/my-notes/blob/main/assets/XSS/2.png)

We can try to type in a script tag into the search query.

![mafia](https://github.com/Jardhyx/my-notes/blob/main/assets/XSS/3.png)

It seems that something is preventing the search from running. If we shorten the search query to simply `search?q=script`, we get the same error. Thus we can infer that having the word "script" in the query will prevent it from running.

From the error message we can see that "q" is a parameter of some sort. "q" can also be found in the search query. If we try to modify the URL to `search?test=script`, we can see that the message changed accordingly.

![mafia](https://github.com/Jardhyx/my-notes/blob/main/assets/XSS/4.png)

## Solution

1. We can modify "q" to be a script tag, in which case would cause the HTML to view it as a script to be executed. We must also encrpyt the word "alert" to prevent it from being filtered.

2. Thus, we can modify the URL to be `search?<script>\u0061lert("xss_by_sam_tan")</script>=script`.