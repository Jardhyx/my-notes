# Faster than Light

It seems that comments are being removed by a script. Thus, we can infer that the password is hidden somewhere in the comments found in the HTML.

## Solution

> Solution may differ based on the browser used. I am using microsoft edge.

1. Using devtools, we can navigate to the network panel, and use `ctrl` + `r` to start recording the network activity.

2. At the very top should be the response for the HTML when the page first loads.

3. We can look for comments in this HTML, where the password is hidden. The password found is `i_weave_light`.