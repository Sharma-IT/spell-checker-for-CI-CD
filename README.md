# Spell Checker for CI/CD

This project provides a simple way to set up a spell checking CI job for your project or application. It uses `codespell` to check for common spelling mistakes in your code and other text files. https://github.com/codespell-project/actions-codespell does exist, however this projects provides a more comprehensive way to use Codespell as a CI check, as it also includes a way to, and documents how to set-up and run Codespell locally, as you'll need to do so to automatically write changes that Codespell recommends. You may also want to opt to integrate a spell checking dependency such as `cspell` with `eslint`, but even that has it's limitations such as not being able to scan markdown files.

## Dependencies

- Python - high-level, general-purpose programming language
- `pnpm` - Fast, disk space efficient package manager. Can be installed with either `npm` or `yarn`
- `codespell` - Spell checker for source code. Has to be installed with `pip`

## Usage

This project is built for a monorepo structure and uses a GitHub Action for running the checks. However, it can be adapted to other development styles and repository structures.

###  Setup

1. Move all the files and scripts in this repository to the repository of your project.
2. For further instructions, refer to `tooling/codespell/docs/usage.md`.

This will set up a GitHub Action that runs the spell checker on every push and pull request. The action will check all files in your repository, excluding certain directories and file types specified in the respective script and words in the `ignore-these-words.txt`.

## Contributing

If you find any issues or have suggestions for improvements, feel free to open an issue or submit a pull request.
