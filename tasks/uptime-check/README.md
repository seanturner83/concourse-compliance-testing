# Uptime Check task

Checks to see if the URLs for the given projects are available.

## Local usage

This assumes a [Concourse](http://concourse.ci/) target named `lite`. Do the following from the top level of this repository.

1. Run the [`filter-team-data`](../filter-team-data/) task.
1. Run

    ```bash
    fly execute -t lite -c tasks/uptime-check/task.yml -i scripts=. -i filtered-projects=out
    ```

## Automated tests

Execute the following from this directory:

```bash
npm install
mocha
```