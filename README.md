# Dev Container Features

'Features' are self-contained units of installation code and development container configuration. Features are designed
to install atop a wide-range of base container images.

Missing a CLI or language in your otherwise _perfect_ container image? Add the relevant Feature to the `features`
property of a [`devcontainer.json`](https://containers.dev/implementors/json_reference/#general-properties). A
[tool supporting the dev container specification](https://containers.dev/supporting) is required to build a development
container.

You may learn about Features at [containers.dev](https://containers.dev/implementors/features/), which is the website for the dev container specification.

## Features

Below are the features currently available in this repository:

| Feature Name | Description                                                                                                                                                                                |               Documentation                |
| ------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | :----------------------------------------: |
| Terratag     | Terratag is a CLI tool allowing for tags or labels to be applied across an entire set of OpenTofu/Terraform files. Terratag will apply tags or labels to any AWS, GCP and Azure resources. | [📚 Link](./src/terratag/) |

'Features' are self-contained units of installation code and development container configuration. Features are designed
to install atop a wide-range of base container images.

## Usage

To reference a Feature from this repository, add the desired Features to a `devcontainer.json`. Each Feature has a `README.md` that shows how to reference the Feature and which options are available for that Feature.

The example below installs the`terratag` feature declared in the [`./src`](./src) directory of this
repository.

See the relevant Feature's README for supported options.

```jsonc
"name": "my-project-devcontainer",
"image": "mcr.microsoft.com/devcontainers/base:ubuntu",  // Any generic, debian-based image.
"features": {
    "ghcr.io/git-saj/devcontainer-features/terratag:1": {}
  }
}
```
