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
     * Also many other inputs, that can be reviewed from the respective action github repo.

### Workflow:
 * in the section `on.pus.paths`,  If you define a path with the ! character, you must also define at least one path without the ! character. If you only want to exclude paths, use paths-ignore instead. Else with only exclude paths, `paths-ignore` can be used.
 * [Default Env Variables](https://docs.github.com/en/actions/learn-github-actions/environment-variables#default-environment-variables) can be used in the workflow.
   * GITHUB_SHA | GITHUB_WORKSPACE | etc
 
### Examples:

* [Multiline-Shell-Commands](.github/workflows/multiline-shell-command.yaml)
  * Single & multiple lined shell commands executed on ubuntu runner
  * 



### Reference: 
* [Link-1](https://github.com/alialaa/github-actions-course/blob/master/.github/workflows/simple.yml)
* [Link-2]()
* [Actions-List](https://github.com/actions)
* 
