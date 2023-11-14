# Phylum CircleCI Orb

The Phylum Orb allows for automatic analysis of your lockfiles and manifests for
vulnerable dependencies.

## Usage

You can find the Phylum Orb on the [CircleCI Orb Registry Page].

[CircleCI Orb Registry Page]: https://circleci.com/developer/orbs/orb/phylum-dev/phylum

To use the Phylum Orb, add your Phylum API token as an environment variable
named `PHYLUM_API_KEY` and add the following job to your workflow:

```yml
version: 2.1
orbs:
  phylum: phylum-dev/phylum@1.0.0
workflows:
  test:
    jobs:
      - phylum/analyze:
          api_key: ${PHYLUM_API_KEY}
```
