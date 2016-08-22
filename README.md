# bare
A minimal ansible-like way to run BAsh commands on REmote machines over SSH.


# Usage
```
./bare script.sh sshUsername hosts.txt
```
OR you can pipe the hosts directly to the command
```
cat hosts.txt | ./bare script sshUsername
```

- **sshUsername**: username to use to ssh to the hosts in the hosts file.
- **hosts.txt**: is txt file that should have a single IP or hostname per line.
- **script.sh**: is a bash file that contains a function with the name bare_func
    whatever inside that function will run remotley on the machines defined in hosts.txt.

# Example:
```
./bare ls.sh hosts.txt klafi
```
`ls.sh` and `hosts.txt` are in the [example](https://github.com/lafikl/bare/tree/master/example) directory in this repo.




---
MIT License

Copyright (c) 2016 Khalid Lafi

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
