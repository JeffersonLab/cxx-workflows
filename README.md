# cxx-workflows
GitHub action C/C++ workflows

| Name                 | Description                      |
|----------------------|----------------------------------|
| [gh-pages-publish.yml](https://github.com/JeffersonLab/cxx-workflows/blob/main/.github/workflows/gh-pages-publish.yml) | Publish API docs to GitHub Pages |
| [gh-release.yml](https://github.com/JeffersonLab/cxx-workflows/blob/main/.github/workflows/gh-release.yml) | Create a GitHub Release |
| [unit-ci.yml](https://github.com/JeffersonLab/cxx-workflows/blob/main/.github/workflows/unit-ci.yml) | Build and run Unit tests (on Linux, Mac, and Windows) |

## Build

```
cmake -S. -Bbuild
cmake --build build
ctest --test-dir build -C Debug -V
```
