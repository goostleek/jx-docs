---
date: 2019-02-03T20:33:47Z
title: "jx create archetype"
slug: jx_create_archetype
url: /commands/jx_create_archetype/
---
## jx create archetype

Create a new app from a Maven Archetype and import the generated code into Git and Jenkins for CI/CD

### Synopsis

Creates a new Maven project using an Archetype 

You then get the option to import the generated source code into a Git repository and Jenkins for CI/CD

```
jx create archetype [flags]
```

### Examples

```
  # Create a new application from a Maven Archetype using the UI to choose which archetype to use
  jx create archetype
  
  # Creates a Camel Archetype, filtering on the archetypes containing the text 'spring'
  jx create archetype --filter-group  org.apache.camel.archetypes --filter-artifact spring
```

### Options

```
  -a, --artifact string                The artifact ID for the new application
  -b, --batch-mode                     In batch mode the command never prompts for user input
      --branches string                The branch pattern for branches to trigger CI/CD pipelines on
  -c, --catalog string                 The Maven Archetype Catalog to use (default "http://central.maven.org/maven2/archetype-catalog.xml")
      --credentials string             The Jenkins credentials name used by the job
      --disable-updatebot              disable updatebot-maven-plugin from attempting to fix/update the maven pom.xml
      --docker-registry-org string     The name of the docker registry organisation to use. If not specified then the Git provider organisation will be used
      --dry-run                        Performs local changes to the repo but skips the import into Jenkins X
      --external-jenkins-url string    The jenkins url that an external git provider needs to use
      --filter-artifact string         Either the Artifact ID or a text filter of the artifact IDs to pick from
  -f, --filter-group string            Filter the Group IDs to choose from for he Archetypes
      --filter-version string          The Version of the Archetype to use
      --git-api-token string           The Git API token to use for creating new Git repositories
      --git-private                    Create new Git repositories as private
      --git-provider-kind string       Kind of Git server. If not specified, kind of server will be autodetected from Git provider URL. Possible values: bitbucketcloud, bitbucketserver, gitea, gitlab, github, fakegit
      --git-provider-url string        The Git server URL to create new Git repositories inside (default "https://github.com")
      --git-username string            The Git username to use for creating new Git repositories
  -g, --group string                   The group ID for the new application (default "com.example")
      --group-ids stringArray          The Group ID of the Archetypes to pick
      --headless                       Enable headless operation if using browser automation
  -h, --help                           help for archetype
      --import-commit-message string   Specifies the initial commit message used when importing the project
      --install-dependencies           Should any required dependencies be installed automatically
  -i, --interactive                    Allow interactive input into the maven archetype:generate command
      --jenkinsfile string             The name of the Jenkinsfile to use. If not specified then 'Jenkinsfile' will be used
      --list-packs                     list available draft packs
      --log-level string               Logging level. Possible values - panic, fatal, error, warning, info, debug. (default "info")
      --name string                    Specify the Git repository name to import the project into (if it is not already in one)
      --no-brew                        Disables the use of brew on macOS to install or upgrade command line dependencies
      --no-draft                       Disable Draft from trying to default a Dockerfile and Helm Chart
      --no-import                      Disable import after the creation
      --no-jenkinsfile                 Disable defaulting a Jenkinsfile if its missing
      --org string                     Specify the Git provider organisation to import the project into (if it is not already in one)
  -o, --output-dir string              Directory to output the project to. Defaults to the current directory
      --pack string                    The name of the pack to use
  -p, --pick                           Provide a list of versions to choose from
      --pull-secrets string            The pull secrets the service account created should have (useful when deploying to your own private registry): provide multiple pull secrets by providing them in a singular block of quotes e.g. --pull-secrets "foo, bar, baz"
      --skip-auth-secrets-merge        Skips merging a local git auth yaml file with any pipeline secrets that are found
      --verbose                        Enable verbose logging
  -v, --version string                 The version for the new application (default "1.0-SNAPSHOT")
```

### SEE ALSO

* [jx create](/commands/jx_create/)	 - Create a new resource

###### Auto generated by spf13/cobra on 3-Feb-2019
