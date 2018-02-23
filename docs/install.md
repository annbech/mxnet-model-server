# Installing MMS
You can install Model Server for Apache MXNet (MMS) either with pip or from source code. If you plan to use MMS for development, install it from source code.


## Prerequisites
Before installing MMS, install the following:
* **Python**: Required. MMS works with Python 2 or 3. To prevent conflicts with your other MXNet or Open Neural Network Exchange (ONNX) installations, you might also want to use a Conda environment. For more information, see [Managing environments](https://conda.io/docs/user-guide/tasks/manage-environments.html) in the *Conda User Guide*.
* **protoc**: Optional. If you plan to use the ONNX features, install the [protobuf compiler](https://github.com/onnx/onnx#installation) *before* installing MMS.
* **Curl**: Optional. We use Curl in all of the examples. Install it with the package manager of your choice.
* **Unzip**: Optional. To easily extract model files and inspect their contents, use Unzip. Associate files with `.model` extensions.

## Install MMS with pip

After installing Python, run the following command:

```bash
pip install mxnet-model-server
```

If you're upgrading from a previous version of MMS, run this command:

```bash
pip install -U mxnet-model-server
```


## Install MMS from Source Code

To install from source code:

1. Clone MMS from the source:

  ```bash
  git clone https://github.com/awslabs/mxnet-model-server.git && cd mxnet-model-server
  ```

2. Install MMS from source code:
```bash
pip install .
```

To upgrade from source code, run this command:
```bash
pip install -U .
```


## Development Installation

If you plan to develop with MMS and change some of the source code, use the `-e` option.

To install MMS from source code and make your changes executable, run this command:

```bash
pip install -e .
```

To upgrade from source code and make your changes executable:
```bash
pip install -U -e .
```


## Troubleshooting

| Issue | Platform | Solution |
|---|---|---|
| Could not find "protoc" executable! | Ubuntu |Run `sudo apt-get install protobuf-compiler libprotoc-dev`. |
|   | MacOS | Run `conda install -c conda-forge protobuf`. |
| Missing [LibGFortran](https://gcc.gnu.org/onlinedocs/gfc-internals/LibGFortran.html) library | Ubuntu |Run `apt-get install libgfortran3`. |
|   | Amazon Linux | Run `yum install gcc-gfortran`. |
