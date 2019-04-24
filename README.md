# **wexpect**

*Wexpect* is a Windows variant of [pexpect](https://pexpect.readthedocs.io/en/stable/).

*Pexpect* is a Python module for spawning child applications and controlling
them automatically.

## **Install**

    pip install wexpect
    
Note that only python 2.x is supported.
    
## **Usage**

To interract with a child process use `spawn` method:

    child = pexpect.spawn('C:\Windows\System32\cmd.exe')
    child.expect('>')
    child.sendline('ls')
    child.expect('>')

For more information see [examples](./examples) folder.

---
## What is it?

Wexpect is a Python module for spawning child applications and controlling
them automatically. Wexpect can be used for automating interactive applications
such as ssh, ftp, passwd, telnet, etc. It can be used to a automate setup
scripts for duplicating software package installations on different servers. It
can be used for automated software testing. Wexpect is in the spirit of Don
Libes' Expect, but Wexpect is pure Python. Other Expect-like modules for Python
require TCL and Expect or require C extensions to be compiled. Wexpect does not
use C, Expect, or TCL extensions. 

Original Pexpect should work on any platform that supports the standard Python pty module. While
Wexpect works on Windows platforms. The Wexpect interface focuses on ease of use so that simple
tasks are easy.


### History

Wexpect is a one-file code developed at University of Washington. There are several
[copy](https://gist.github.com/anthonyeden/8488763) and
[reference](https://mediarealm.com.au/articles/python-pexpect-windows-wexpect/)
to this code with very few (almost none) documentation nor integration.

This repo tries to fix these limitations, with a few example code and pypi integration.


---
## Installation and limitation of wexpect

Current version does *not* work on python-3.x. You need to use **python 2.x** to use wexpect.

### Standard installation

This version is uploaded to pypi server so you can easily install with pip:

    pip install wexpect
    
### Manual installation

Because this is a tiny project dropping the wexpect.py file into your working directory is usually
good enough instead of installing. However in this case you need to install manually the one dependence.

One (non stanbdard) package, **pypiwin32** is needed by wexpect.

    pip install pypiwin32
    