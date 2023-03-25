1.  `bump2version <major|minor|patch>`
2.  wait for CI to create release
3.  do release notes (match style, generate release notes)
4.  (required once) install `build` and `twine` modules
5.  `python3 -m build`
6.  `rm -rf dist/` (cleanup)
7.  https://readthedocs.org/projects/synadm/versions/ and check if docs is
    published/activated
8.  (requires prepared setup) `twine upload -r test-synadm dist/*`
9.  test install `python3 -m pip install --index-url https://test.pypi.org/simple/ --no-deps synadm`
10. if it works, `twine upload --repository synadm dist/*`

done, things has been released.

for step 8, please go generate an API token and setup `~/.pypirc`.
`test-synadm` for test.pypi.org, `synadm` for pypi.org.
