---
date: 2019-02-03T20:33:47Z
title: "jx get workflows"
slug: jx_get_workflows
url: /commands/jx_get_workflows/
---
## jx get workflows

Display either all the available workflows or a specific workflow

### Synopsis

Display either all the workflows or a specific workflow

```
jx get workflows [flags]
```

### Examples

```
  # List all the available workflows
  jx get workflow
  
  # Display a specific workflow
  jx get workflow -n default
```

### Options

```
  -h, --help            help for workflows
  -n, --name string     The name of the workflow to display
  -o, --output string   The output format such as 'yaml'
```

### SEE ALSO

* [jx get](/commands/jx_get/)	 - Display one or more resources

###### Auto generated by spf13/cobra on 3-Feb-2019
