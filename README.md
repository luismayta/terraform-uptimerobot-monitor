<!--


  ** DO NOT EDIT THIS FILE
  **
  ** 1) Make all changes to `README.yaml`
  ** 2) Run`make readme` to rebuild this file.
  **
  ** (We maintain HUNDREDS of open source projects. This is how we maintain our sanity.)
  **


  -->

# terraform-uptimerobot-monitor

[![GitHub tag (latest SemVer)](https://img.shields.io/github/v/tag/hadenlabs/terraform-uptimerobot-monitor.svg?label=latest&sort=semver)](https://github.com/hadenlabs/terraform-uptimerobot-monitor/releases) [![Lint](https://github.com/hadenlabs/terraform-uptimerobot-monitor/actions/workflows/lint.yml/badge.svg?branch=develop)](https://github.com/hadenlabs/terraform-uptimerobot-monitor/actions) [![Issues](https://img.shields.io/github/issues/hadenlabs/terraform-uptimerobot-monitor.svg)](https://github.com/hadenlabs/terraform-uptimerobot-monitor/issues) [![Latest Release](https://img.shields.io/github/release/hadenlabs/terraform-uptimerobot-monitor.svg)](https://github.com/hadenlabs/terraform-uptimerobot-monitor/releases)

terraform uptimerobot monitor

## Usage

```hcl
  module "main" {
    source = "hadenlabs/monitor/uptimerobot"
    version   = "0.1.0"
    monitors = [
      {
        friendly_name = "test-url"
        url           = "https://google.com"
      },
    ]
  }

```

Full working examples can be found in [examples](./examples) folder.

## Examples

### basic

```hcl
  module "main" {
    source = "hadenlabs/monitor/uptimerobot"
    version   = "0.1.0"
    source = "git://github.com/hadenlabs/terraform-uptimerobot-monitor.git?ref=0.1.0"
    monitors = [
      {
        friendly_name = "test-url"
        url           = "https://google.com"
      },
    ]
  }
```

 <!-- BEGIN_TF_DOCS -->

## Requirements

| Name                                                                           | Version |
| ------------------------------------------------------------------------------ | ------- |
| <a name="requirement_terraform"></a> [terraform](#requirement_terraform)       | >= 0.13 |
| <a name="requirement_uptimerobot"></a> [uptimerobot](#requirement_uptimerobot) | >=0.5.1 |

## Providers

| Name                                                                     | Version |
| ------------------------------------------------------------------------ | ------- |
| <a name="provider_uptimerobot"></a> [uptimerobot](#provider_uptimerobot) | >=0.5.1 |

## Modules

No modules.

## Resources

| Name | Type |
| --- | --- |
| [uptimerobot_monitor.this](https://registry.terraform.io/providers/louy/uptimerobot/latest/docs/resources/monitor) | resource |

## Inputs

| Name | Description | Type | Default | Required |
| --- | --- | --- | --- | :-: |
| <a name="input_monitors"></a> [monitors](#input_monitors) | The list of UptimeRobot monitors | `list(map(string))` | n/a | yes |

## Outputs

| Name                                                        | Description       |
| ----------------------------------------------------------- | ----------------- |
| <a name="output_ids"></a> [ids](#output_ids)                | show ids instance |
| <a name="output_instance"></a> [instance](#output_instance) | show instance     |

<!-- END_TF_DOCS -->

## Help

**Got a question?**

File a GitHub [issue](https://github.com/hadenlabs/terraform-uptimerobot-monitor/issues).

## Contributing

### Bug Reports & Feature Requests

Please use the [issue tracker](https://github.com/hadenlabs/terraform-uptimerobot-monitor/issues) to report any bugs or file feature requests.

### Development

In general, PRs are welcome. We follow the typical "fork-and-pull" Git workflow.

1.  **Fork** the repo on GitHub
2.  **Clone** the project to your own machine
3.  **Commit** changes to your own branch
4.  **Push** your work back up to your fork
5.  Submit a **Pull Request** so that we can review your changes

**NOTE:** Be sure to rebase the latest changes from "upstream" before making a pull request!

## Module Versioning

This Module follows the principles of [Semantic Versioning (SemVer)](https://semver.org/).

Using the given version number of `MAJOR.MINOR.PATCH`, we apply the following constructs:

1. Use the `MAJOR` version for incompatible changes.
1. Use the `MINOR` version when adding functionality in a backwards compatible manner.
1. Use the `PATCH` version when introducing backwards compatible bug fixes.

### Backwards compatibility in `0.0.z` and `0.y.z` version

- In the context of initial development, backwards compatibility in versions `0.0.z` is **not guaranteed** when `z` is increased. (Initial development)
- In the context of pre-release, backwards compatibility in versions `0.y.z` is **not guaranteed** when `y` is increased. (Pre-release)

## Copyright

Copyright © 2018-2021 [Hadenlabs](https://hadenlabs.com)

## Trademarks

All other trademarks referenced herein are the property of their respective owners.

## License

The code and styles are licensed under the LGPL-3.0 license [See project license.](LICENSE).

## Don't forget to 🌟 Star 🌟 the repo if you like terraform-uptimerobot-monitor

[Your feedback is appreciated](https://github.com/hadenlabs/terraform-uptimerobot-monitor/issues)
