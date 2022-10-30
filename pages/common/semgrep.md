# semgrep

> Perform static source code analysis (SAST) to detect security vulnerabilities.
> It is a SAST tool aiming to minimize false positives and being fast enough to be used in CI pipelines.
> More information: <https://semgrep.dev/docs/cli-reference/>.

- Run on a source directory, automatically detecting matching rules:

`semgrep --config=auto {{path/to/directory}}`

- Run on a source directory, manually selecting the desired rulesets:

`semgrep --config p/{{ruleset_name1}} --config p/{{ruleset_name2}} {{path/to/directory}}`

- Run within a Docker container on the current directory:

`docker run --rm -v "${PWD}:/src" returntocorp/semgrep [--config p/{{ruleset_name}} ...]`