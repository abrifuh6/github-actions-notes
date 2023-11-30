# GitHub Actions Notes

## Agenda

- GitHub actions
- Actions & CI
- CD & Release management
- Self-hosted runners
- Build management
- Package Management
- Secrets Management

## Actions Advantages

- Fully integrated with github
- Respond to any github event(full automation engine)
- Community-powered workflows
- Any platform, any language and any cloud

## Key functionalities

- Can be ran on any systems like Linux, MacOs, Windows and Containers.
- Matrix builds
- Streaming, searchable, linkable logs.
- Built-in secret store.
- Easy to write, easy to share.

## Components of an Action

- How does an Action work?

![image](github-actions.png)

As you can see from the image above, events trigger the workflows.

 These workflows are set of tasks or actions .

## 1. Events

- First part specified in the yaml. It will be something like,

```yaml
on:
  schedule:
  - cron: 0 12 * * 1
```

- Some other github triggered events:
  - push, pull_request, public
  - Manually triggered:
    - worklfow_dispatch(external systems)

## 2. Workflows

- Workflows are like pipelines in jenkins, teamcity etc.
- Codify useful, customized proccesses.
- .yaml syntax
- .github/workflows (this is where you need to add your workflows folder)

workflow files glue together existing actions in sequence. 

- listen for particular events
- Then run pre-existing actions
- or shell scripts

- Actions run in VMs (Linux, Win, Mac)
  - or Docker on Linux vm
- Logs streaming & artifacts
- Secret store with each repo or organization. 

## 3. Actions

- Reusable units of code
- Referencing vs authoring actions
- Administrative features
  - It's adviced not to limit actions on the market place, instead, a code review should be done after an actions from marketplace is used.
- Storing shared Actions
  - If you decide to share actions, the repo must be plublic.
- Post your Actions to the GitHub market place.

| 