---
layout: default
---

Upincoming CyberSec Professional

https://www.linkedin.com/in/paris-wright-57342b263 

#README
With a strong dedication to the cybersecurity field, I’m pursuing my studies at college while consistently expanding my skill set through industry-recognized certifications. These credentials have equipped me with foundational knowledge in areas like network security, threat detection, and vulnerability management. They also enhance my understanding of the latest technologies and best practices, allowing me to tackle complex security challenges with confidence.

Alongside my academic coursework, I stay up-to-date with emerging trends and threats in cybersecurity. This includes exploring cutting-edge topics, such as ethical hacking and incident response, to build a well-rounded skill set. My goal is to leverage this knowledge and hands-on experience to secure digital environments, defend against cyber threats, and ultimately contribute to a safer digital world.

# Basic htmlvproject that verifies a persons age to confirm whether they are an adult or minor. 

<!DOCTYPE html>
<html lang="en">
<head>
    <title>Age Verification</title>
</head>
<body>
    <h1>Age Verification</h1>
    <p id="message"></p>

    <script>
        age = prompt("What is your age")
        if (age >= 18) {
            document.getElementById("message").innerHTML = "You are an adult.";
        } else {
            document.getElementById("message").innerHTML = "You are a minor.";
        }
    </script>
</body>
</html>

## Python project that verifies an employee

#!/usr/bin/env python3

import re

def validate_user(username, minlen):
    """Checks if the received username matches the required conditions."""
    if type(username) != str:
        raise TypeError("username must be a string")
    if minlen < 1:
        raise ValueError("minlen must be at least 1")
    
    # Usernames can't be shorter than minlen
    if len(username) < minlen:
        return False
    # Usernames can only use letters, numbers, dots and underscores
    if not re.match('^[a-z0-9._]*$', username):
        return False
    # Usernames can't begin with a number
    if username[0].isnumeric():
        return False
    return True

### misc projects

```python

"""A simple Hello World type app which can serve on port 8000.
Optionally, a different port can be passed.

The code was inspired by:
https://gist.github.com/davidbgk/b10113c3779b8388e96e6d0c44e03a74
"""
import http
import http.server
import socket
import socketserver
import sys

# TCP port for listening to connections, if no port is received
DEFAULT_PORT=8000

class Handler(http.server.SimpleHTTPRequestHandler):
    def do_GET(self):
        self.send_response(http.HTTPStatus.OK)
        self.end_headers()
        # Hello message
        self.wfile.write(b'Hello Cloud')
        # Now get the hostname and IP and print that as well.
        hostname = socket.gethostname()
        host_ip = socket.gethostbyname(hostname)
        self.wfile.write(
            '\n\nHostname: {} \nIP Address: {}'.format(
                hostname, host_ip).encode())


def main(argv):
    port = DEFAULT_PORT
    if len(argv) > 1:
        port = int(argv[1])

    web_server = socketserver.TCPServer(('', port), Handler)
    print("Listening for connections on port {}".format(port))
    web_server.serve_forever()


if __name__ == "__main__":
    main(sys.argv)

```

```python
def git_opeation():
 print("I am adding example.py file to the remote repository.")
git_opeation()
```

#### Header 4

*   This is an unordered list following a header.
*   This is an unordered list following a header.
*   This is an unordered list following a header.

##### Header 5

1.  This is an ordered list following a header.
2.  This is an ordered list following a header.
3.  This is an ordered list following a header.

###### Header 6

| head1        | head two          | three |
|:-------------|:------------------|:------|
| ok           | good swedish fish | nice  |
| out of stock | good and plenty   | nice  |
| ok           | good `oreos`      | hmm   |
| ok           | good `zoute` drop | yumm  |

### There's a horizontal rule below this.

* * *

### Here is an unordered list:

*   Item foo
*   Item bar
*   Item baz
*   Item zip

### And an ordered list:

1.  Item one
1.  Item two
1.  Item three
1.  Item four

### And a nested list:

- level 1 item
  - level 2 item
  - level 2 item
    - level 3 item
    - level 3 item
- level 1 item
  - level 2 item
  - level 2 item
  - level 2 item
- level 1 item
  - level 2 item
  - level 2 item
- level 1 item

### Small image

![Octocat](https://github.githubassets.com/images/icons/emoji/octocat.png)

### Large image

![Branching](https://guides.github.com/activities/hello-world/branching.png)


### Definition lists can be used with HTML syntax.

<dl>
<dt>Name</dt>
<dd>Godzilla</dd>
<dt>Born</dt>
<dd>1952</dd>
<dt>Birthplace</dt>
<dd>Japan</dd>
<dt>Color</dt>
<dd>Green</dd>
</dl>

```
Long, single-line code blocks should not wrap. They should horizontally scroll if they are too long. This line should be long enough to demonstrate this.
```

```
The final element.
```
