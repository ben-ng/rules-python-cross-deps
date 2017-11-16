To Reproduce
------------

This works:

```sh
cat test-requirements.txt | xargs -n1 pip install
python test.py
```

Then clean up:

```sh
pip freeze | xargs pip uninstall -y
```

This does not work:

```sh
bazel test //...
```

word2vec fails to build because it can't find Cython or `backports.ssl_match_hostname`, although they're declared in its `requirements.txt`.

```txt
ImportError: No module named Cython.Build
```

