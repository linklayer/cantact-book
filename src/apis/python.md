# Python

A Python API is implemented by the CANtact driver. This can be used directly, but it is recommended to use 
the `python-can` library. The `develop` branch of `python-can` is required to use the command line utilities.

Install `cantact` and `python-can`:

```
python3 -m pip -U pip
python3 -m pip install cantact
git clone https://github.com/hardbyte/python-can.git
cd python-can
python -m pip install .
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
