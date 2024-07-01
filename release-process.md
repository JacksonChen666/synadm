1.  `bump2version --no-tag <major|minor|patch>`
2.  create your own tag with a shortlog (tag version must match specified
    version)
3.  (required once) install `build` and `twine` modules
4.  `rm -r dist/` (cleanup)
5.  `python3 -m build`
6.  push with `--follow-tags`
7.  wait for CI to create release
8.  do release notes (match style, generate release notes)
9.  publish release
10. `twine upload --repository pypi dist/*`
11. https://readthedocs.org/projects/synadm/versions/ and check if docs is
    published/activated

done, things has been released.

for step 10, please go generate an API token and setup `~/.pypirc`.
`testpypi` for test.pypi.org, `pypi` for pypi.org.

`~/.pypirc` should be this
(https://packaging.python.org/en/latest/specifications/pypirc/#common-configurations):

```
[distutils]
index-servers =
    pypi
    testpypi

[pypi]
repository = https://upload.pypi.org/legacy/
username = __token__

[testpypi]
repository = https://test.pypi.org/legacy/
username = __token__
```

password saved in keyring, do as following:
```
keyring set https://upload.pypi.org/legacy/ __token__
keyring set https://test.pypi.org/legacy/ __token__
```
use API tokens, not passwords. MFA will prevent password use... eventually

ref: https://packaging.python.org/en/latest/specifications/pypirc/#using-another-package-index
