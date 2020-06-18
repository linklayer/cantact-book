# ISOTP

The can-utils package contains tools for working with ISOTP. However, the kernel ISOTP support needed by these tools is not available by default on most systems. This results in an `Protocol not supported` error when running ISOTP tools.

The can-isotp kernel module and build instructions are available [on Github](https://github.com/hartkopp/can-isotp)

## Testing ISOTP Driver

To use ISOTP, you will need two physically connected CAN channels (or gatewayed virtual CAN devices) to send and receive data. Once set up, start `isotprecv`:
```
isotprecv -s456 -d123 can1
```

In another terminal, run `isotpsend` to send ISOTP data. This tool reads from standard input, so `echo` is used to provided data as a sequence of space seperated hexidecimal bytes:
```
echo "de ad be ef de ad be ef aa bb cc dd" | isotpsend -s123 -d456 can0 
```

The data should appear in `isotprecv`.
