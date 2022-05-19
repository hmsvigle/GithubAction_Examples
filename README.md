# Github Action Examples

Sample examples of Github Action

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

## Examples:

* [Multiline-Shell-Commands](.github/workflows/multiline-shell-command.yaml)
  * Single & multiple lined shell commands executed on ubuntu runner
  * 



Reference: 
* [Link-1](https://github.com/alialaa/github-actions-course/blob/master/.github/workflows/simple.yml)
* [Link-2]()
