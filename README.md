# cxx-workflows
GitHub action C/C++ workflows

## Reusable workflows

| Name                 | Description                      |
|----------------------|----------------------------------|
| [gh-pages-publish.yml](https://github.com/JeffersonLab/cxx-workflows/blob/main/.github/workflows/gh-pages-publish.yml) | Publish API docs to GitHub Pages |
| [gh-release.yml](https://github.com/JeffersonLab/cxx-workflows/blob/main/.github/workflows/gh-release.yml) | Create a GitHub Release |
| [unit-ci.yml](https://github.com/JeffersonLab/cxx-workflows/blob/main/.github/workflows/unit-ci.yml) | Build and run Unit tests (on Linux, Mac, and Windows) |

## How to use
This project uses it's own workflows in order to test them (the C++ App/Lib is just a demo/example).  Copy and paste one or more of the following files into your project `.github/workflows` directory and update parameters accordingly:

| Name                 | Description                      |
|----------------------|----------------------------------|
| [cd.yml](https://github.com/JeffersonLab/cxx-workflows/blob/main/.github/workflows/cd.yml) | Continuous Deployment of an App/Lib with GitHub release |
| [dd.yml](https://github.com/JeffersonLab/cxx-workflows/blob/main/.github/workflows/ci.yml) | Continuous Integration of an App/Lib |

## Demo App
This project includes a `Hello World` C++ app to demonstrate the workflow.  Use the [cxx-devcontainer](https://github.com/JeffersonLab/cxx-devcontainer) to build:

```
cmake -S. -Bbuild
cmake --build build
ctest --test-dir build -C Debug -V
```
