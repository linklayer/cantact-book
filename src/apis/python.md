# Python

A Python API is implemented by the CANtact driver. This can be used directly, but it is recommended to use 
the `python-can` library. Both components can be installed using `pip`:

```
python3 -m pip -U pip
python3 -m pip install cantact git+https://github.com/ericevenchick/python-can@cantact
```

If no binary release exists for your platform, the driver can be built manually. 
For details, see the [README](https://github.com/linklayer/cantact/#building-python-support).

Once CANtact and `python-can` are installed, the bundled tools can be used. For example,
to log frames on CAN 0 at 500000 kbit/s:

```
can_logger.py -i cantact -c 0 -b 500000
```

## Examples

Examples of using the Python API directly and through `python-can` are 
[available on Github](https://github.com/linklayer/cantact/tree/master/driver/examples).