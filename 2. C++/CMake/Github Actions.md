**MOC**:: [[2. C++ MOC]]
**Tags**:: #cplusplus #cmake 

# About
Github Action run workflow (defined in `.github/actions.yml` by default) on CI pipeline. Example file can be found [here](). Workflow in this setup do:
1. download dependencies
2. init conan
3. run unit tests
4. print code coverage.
CI pipeline run at each push, on branch who is specified in `actions.yml` file.