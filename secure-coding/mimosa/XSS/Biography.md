# Biography

The idea is that we need to cause an alert in the webpage without using the script tag.

We can first explore the website for any vulnerabilities using devtools. If we navigate to the about me page, notice that the URL changes to `about?img=dog.jpg`. If we modify the URL to `about?img=dog.jpg" "test`, we can see that the 'img src' changes accordingly.

![html](https://github.com/Jardhyx/my-notes/blob/main/assets/XSS/1.png)

Thus, we can infer that the image source is related to the URL.

## Solution

1. Since we know that we can change the contents of 'img src' through the URL, we can modify it to show an alert on error.

2. Modify the URL to `about?img=dog.jpg" onerror='alert("ethan_was_here")'`

> Optional: To display the alert, we can make the webpage look for a non-existent image by editing the 'dog.jpg' to 'dg.jpg' or anything of the sort.