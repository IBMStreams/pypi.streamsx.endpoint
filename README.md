# pypi.streamsx.endpoint

This exposes SPL operators in the `com.ibm.streamsx.inetserver` toolkit as Python methods.

Package is organized using standard packaging to upload to PyPi.

The package is uploaded to PyPi in the standard way:
```
cd package
python setup.py sdist bdist_wheel upload -r pypi
```
Note: This is done using the `ibmstreams` account at pypi.org and requires `.pypirc` file containing the credentials in your home directory.

Package details: https://pypi.python.org/pypi/streamsx.endpoint

Documentation is using Sphinx and can be built locally using:
```
cd package/docs
make html
```

or

    ant doc

and viewed using
```
firefox package/docs/build/html/index.html
```

The documentation is also setup at `readthedocs.io`.

Documentation links:
* http://streamsxendpoint.readthedocs.io/

## Version update

To change the version information of the Python package, edit following files:

- ./package/docs/source/conf.py
- ./package/streamsx/endpoint/\_\_init\_\_.py

When the development status changes, edit the *classifiers* in

- ./package/setup.py

When the documented sample must be changed, change it here:

- ./package/streamsx/endpoint/\_\_init\_\_.py
- ./package/DESC.txt


## Test

Run the test with:

    ant test
