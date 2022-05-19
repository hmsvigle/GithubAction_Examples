# Github Action Examples

## Overview:

* Multiple jobs can run on diff runners `parallelly`
* The yaml structure is ideally in below format.

````yaml

Workflow:
  * on Event:
    * Job-1:
      * Step-1:
      * Step-2:
    * Job-2:
      * Step-1:
      * Step-2:
````
* We can sepcify `needs` snippet for sequential execution of jobs.

```yaml
 
 Workflow:
  * on Event:
    * Job-1:
      * Step-1:
    * Job-2:
        runs-on: [ubuntu-latest]
        # For Sequencial execution
        needs: ["Job-1"]
      * Step-1:
 ```
 * **`Steps`** can execute `Commands`/`Actions`
   * Syntax conatins few parameters:
     * uses: <org>/<repo_name>@<release> i.e `actions/hello-world-javascript-action@v1` from the [link](https://github.com/actions/hello-world-javascript-action)
     * with: Takes inputs
     * id: we can define a id for this step. so that output can be referenced in a different step.

### Examples:

* [Multiline-Shell-Commands](.github/workflows/multiline-shell-command.yaml)
  * Single & multiple lined shell commands executed on ubuntu runner
  * 



Reference: 
* [Link-1](https://github.com/alialaa/github-actions-course/blob/master/.github/workflows/simple.yml)
* [Link-2]()
* [Actions-List](https://github.com/actions)
* 
