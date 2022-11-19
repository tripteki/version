<h1 align="center">Convention</h1>

Trip Teknologi's Semantic Version Convention.

Getting Started
---

How to use :

- You need to create a workflow in `.github/workflows/`.

    Sample file :

    ```
    name: Semantic Version

    on: push

    jobs:
        version:
            runs-on: ubuntu-latest
            steps:
                - id: tripteki
                  uses: tripteki/version@1.0.0
                  with:
                    token: ${{ secrets.GITHUB_TOKEN }}
                    artifact: <artifact>.<extension>
                - shell: sh
                  run: |
                    echo ${{ steps.tripteki.outputs.exists }}
                    echo ${{ steps.tripteki.outputs.version }}
                    echo ${{ steps.tripteki.outputs.passes }}
    ```

- You have to modify `artifact` section to targeting artifact version.

Credit
---

- Conventionalcommit ([@conventionalcommit](https://www.conventionalcommits.org))

Author
---

- Trip Teknologi ([@tripteki](https://linkedin.com/company/tripteki))
- Hasby Maulana ([@hsbmaulana](https://linkedin.com/in/hsbmaulana))
