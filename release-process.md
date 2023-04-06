1.  `bump2version --no-tag <major|minor|patch>`
2.  create your own tag with a shortlog
3.  push
4.  wait for CI to create release
5.  do release notes (match style, generate release notes)
6.  publish
7.  (required once) install `build` and `twine` modules
8.  `rm -rf dist/` (cleanup)
9.  `python3 -m build`
10. https://readthedocs.org/projects/synadm/versions/ and check if docs is
    published/activated
11. (requires prepared setup) `twine upload -r test-synadm dist/*`
12. test install
    `python3 -m pip install --index-url https://test.pypi.org/simple/ --no-deps synadm`
13. if it works, `twine upload --repository pypi dist/*`

done, things has been released.

for step 8, please go generate an API token and setup `~/.pypirc`.
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
