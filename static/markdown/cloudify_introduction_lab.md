# Sample Lab

Connect to your lab environment, and run `juju bootstrap` on the deploy node
(the bootstrap process will take a few minutes).

    $ juju bootstrap

Next, let's deploy our first charm, `juju-gui`, to the `deploy` node itself
(this node gets assigned an identifier of "0" by `juju bootstrap`):

    $ juju deploy --config=~/juju-config.yaml juju-gui --to 0

Once deployment is complete, you can connect to the Juju GUI by pointing your
browser to your `deploy` node's public IP address, on port 8080:

    https://PUBLIC_IP_ADDRESS:8080

Your own public IP address is displayed on the terminal window when you get
connected to the lab environment.  To easily retrieve it at a later time,
simply run the following from the terminal:

    $ curl http://icanhazip.com
    77.81.7.129

Your `PUBLIC_IP_ADDRESS` would be, in this case, `77.81.7.129`, so your Juju
GUI would be located at:

[https://77.81.7.129:8080](https://77.81.7.129:8080)

The `deploy` node alone doesn't quite cut it, and that is why your training
environment includes four other nodes: `alice`, `bob`, `charlie`, and `daisy`.
These VMs have these pre-determined private IPs:

* `alice`: 192.168.122.111
* `bob`: 192.168.122.112
* `charlie`: 192.168.122.113
* `daisy`: 192.168.122.114

You will be able to connect to them with SSH using either the IP addresses
mentioned above or their hostnames, by hopping to them via the `deploy` node.

Please SSH into `alice` now.  If asked to verify the alice's host key, type in
"yes":

    $ ssh alice
    ...
    The authenticity of host 'alice (192.168.122.111)' can't be established.
    ECDSA key fingerprint is 1c:56:48:40:2b:e1:59:95:13:9b:6f:ea:f7:d2:bd:3b.
    Are you sure you want to continue connecting (yes/no)? yes

Please SSH into `bob`, `charlie` and `daisy` as well.

Feel free to look around: at this point it is an entirely clean Ubuntu 14.04
cloud image installation.  `bob`, `charlie`, and `daisy` have been similarly
configured.

When you're done, make sure to click the `Check Progress` button: this is how
you'll be graded for these exercises.
