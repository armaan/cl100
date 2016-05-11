# Using the Lab Environment

The lab environment is accessed via the terminal screen embedded below these
instructions. To find it, simply scroll down.

## Overview of the Lab Environment

The lab environment consists of several virtual machines (VMs), or nodes with
the following local IP addresses.

* _deploy_: **`192.168.122.100`**
* _alice_: **`192.168.122.111`**
* _bob_: **`192.168.122.112`**
* _charlie_: **`192.168.122.113`**

The _deploy_ node is the only machine with a publicly available IP address.
Your terminal automatically connects to _deploy_. Use SSH from _deploy_ to hop
to the other nodes.

## SSH Between Nodes

The terminal multiplexer `screen` allows you to open multiple windows and
navigate between them. When you connect to _deploy_, you automatically enter a
`screen` session. We recommend you use multiple terminal windows and connect
each window to a different node.

To connect to _alice_ in a new `screen` window, follow these instructions
using the terminal below:

1. From the _deploy_ node (it's where you start out), press Ctrl+A, release,
   then press C.

2. In this new screen window, SSH into _alice_ by entering:

        $ ssh alice

3. To confirm the authenticity of the host, enter "yes" at the prompt.

4. Try switching between screen windows. Press Ctrl+A, release, then and
   press ". Select the window you want using ↑ or ↓ or press the
   corresponding number, then press Enter. Alternatively, press Ctrl+A,
   release, then press '. Enter the number of the window you want.

5. Repeat steps 1 to 4 for `bob` and `charlie`.

Feel free to look around: at this point these VMs are entirely clean Centos 7
cloud image installations.

When you're done, make sure to click the `Check Progress` button: this is how
you'll be graded for these exercises.
