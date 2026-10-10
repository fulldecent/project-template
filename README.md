# My Fruit Stand

> [!TIP]
> This template is a starting point you can use for every project. We offer:
>
> * Clear structure and quick notes
> * Continuous integration to [check formatting](.github/workflows/lint.yml)
> * Automated releases with [Release Please](.github/workflows/release.yml) and SLSA provenance attestation
> * Modern [EditorConfig](.editorconfig), [.gitignore](.gitignore) and linting
>
> If a more specific template applies, use that instead:
>
> * [Node.js template](https://github.com/fulldecent/node.js-template): Node.js modules (e.g. on NPM) and applications
> * [GitHub Pages template](https://github.com/fulldecent/github-pages-template): collaboratively-edited HTML websites
> * [Swift 6 module template](https://github.com/fulldecent/swift6-module-template): reusable Swift 6 modules
> * [Swift app template](https://github.com/fulldecent/swift-app-template): Xcode apps, including TestFlight and App Store review
> * [Solidity template](https://github.com/fulldecent/solidity-template): Solidity contracts (technology preview)
> * [Moodle plugin template](https://github.com/fulldecent/moodle-local_plugin_template): Moodle plugin (work in progress)
> * [Podcast template](https://github.com/fulldecent/podcast-template): podcast on your own domain
>
> What is in-scope for this template?
>
> We the people who manage projects, in order to surface up records of past decisions and make projects inviting for a growing audience, maintain this starting point for all projects.
>
> This project-template must remain broad—addressing the needs of many kinds of projects. This includes projects related to compiling code as well as others. Every project deserves a README, and a clear rule on basic formatting questions, this is why we include continuous integration linting.
>
> We do not specify that GitHub and GitHub Actions are the only way to host projects, others may consider our GitHub-specific notes as a starting point guide for implementing outside of GitHub.
>
> And now below is the template, shown for a specific hypothetical project, enjoy!

[![Lint](https://github.com/fulldecent/project-template/actions/workflows/lint.yml/badge.svg)](https://github.com/fulldecent/project-template/actions/workflows/lint.yml) [![Build and test](https://github.com/fulldecent/project-template/actions/workflows/build-test.yml/badge.svg)](https://github.com/fulldecent/project-template/actions/workflows/build-test.yml)

Fresh fruit, sold on the corner. Cups, prices, and hours are on the stand.

Our stand offers:

* Simple setup instructions with minimal supplies and tools needed
* Beautiful color theming options to fit your style
* Notes on sanitary food service operations to prepare your staff for go-live

[ Imagine a photo here of staff with an assembled My Fruit Stand servicing customers on a bright sunny day. ]

> [!NOTE]
> After you use the template, replace "My Fruit Stand" and the sentence above with what your project does, and the badge URL. If you can, include screenshots/graphics to fill in that placeholder. Because you have just six seconds to pique a person's interest!

## Try it out

The stand is at the corner of Main and 3rd Streets, Saturdays 10–2. Walk up and pretend to be a normal customer, you'll get the full experience without having to read any further in this introduction.

> [!NOTE]
>If you have a web demo (or "playground", no install required), show that here. If not, delete this section.
>
>A demo allows visitors to quickly feel how your project connects with their needs... and starts them thinking about its value proposition.

## Installation

You will need our PDF guide and materials list to install your own stand based on this project. Our latest guide is available on the [releases page](https://github.com/fulldecent/project-template/releases).

> [!NOTE]
> If your project requires some installation process to use it, explain that here. If not, delete this section.
>
> Other common names for this section include: getting started, setup.
>
> Please consider that people using your project may not care about the technology you build it on. That means explaining those technologies (at least their setup) is in-scope for your project setup instructions.
>
> Examples:
>
> | You offer...                                          | Your audience...                      | Your install section should...                                                                                        |
> | ----------------------------------------------------- | ------------------------------------- | --------------------------------------------------------------------------------------------------------------------- |
> | A QR code scanner library using Node.js (with no CLI) | Must know of Node.js                  | Explain which versions of Node.js are acceptable to run your product.                                                 |
> | A mobile phone app                                    | Has a mobile phone                    | Show how to get the published app binary from the canonical phone app store or other location.                        |
> | A fruit stand kit                                     | May not have a second set of hands    | Explain what qualifications are necessary for their helper (adult? can lift a certain weight?).                       |
>
> Some technologies have offensive install instructions, e.g. `curl|sh`. You should avoid linking to those websites and invest the time to make better instructions for your customers.

## Usage

Running a fruit stand is a lot of fun but also serious work. Each day you show up for work remember to:

1. Check the weather.
2. Check your supplies.
3. Put on your smile and get to work.

> [!NOTE]
> Explain how to use your project. Or link to the canonical usage instructions.
>
> Other common names for this section include: "how to...".

## Development

Thank you for taking an interest in improving our fruit stand and the fruit stands of many people using this project!

Our guides are PDF files that we build using Inkscape. You will need [Inkscape](https://inkscape.org/) version 1.4 or later to work with our editable files.

Please also learn about our theming and text style guide. That way we will be able to use your contributions with less needed rework.

> [!NOTE]
> If your project requires some system configuration process to contribute to your project, explain that here. If not, delete this section.
>
> Other common names for this section include: contributing, get involved. It is a higher level of commitment than just using your product.

### Testing

All project updates that we release must conform to our test suite. We have set our GitHub so that each commit automatically runs these tests and calls out any problems. But you can also run it locally on your computer before you send in commits and pull requests.

If you have an actively maintained version of Node.js installed, you can use this command to correct most formatting issues in your copy of this project. Please do that before sending proposed changes.

```sh
npx prettier@latest --check . --write
npx markdownlint-cli@latest "**/*.md" --fix
```

> [!NOTE]
> Other common names for this section include: validation, checks.

### Releases

Use `fix:`, `feat:` or `BREAKING CHANGE:`  in your commit messages. This will trigger our bot to make a new "release draft" pull request. Merging that pull request triggers a new tag and GitHub Release.

> [!NOTE]
> In your GitHub repository settings, under Actions, General, Workflow permissions, check "Allow GitHub Actions to create and approve pull requests". Release Please needs this to open the release draft pull request.
>
> A repository created from this template starts with no tags and no releases. Release Please reads the latest tag on the default branch to choose the next version. The publish job accepts a tag shaped like `v1.2.3`.
>
> Run these commands from a clone of the new repository. `gh` fills in `{owner}/{repo}` from that clone.
>
> List tags:
>
> ```sh
> gh api repos/{owner}/{repo}/tags --jq '.[].name'
> ```
>
> Set the starting tag on the current `main` commit. `v0.0.0` is the version Release Please counts forward from. Use another `vMAJOR.MINOR.PATCH` tag when this repository should start later.
>
> ```sh
> gh api --method POST repos/{owner}/{repo}/git/refs \
>   -f ref="refs/tags/v0.0.0" \
>   -f sha="$(gh api repos/{owner}/{repo}/commits/main --jq .sha)"
> ```
>
> `gh release list` and `gh release create` publish the releases this workflow creates after that tag.

### Maintenance

The project administrator completes these maintenance tasks each month. If they are 3+ months late, please remind them or send your own issue/pull request.

1. Identify external Actions in [.github/workflows](./.github/workflows) scripts and look for available new versions. Review and then update to the new version if it is safe. GitHub-supported Actions (i.e. under the actions/ organization) may require only cursory review.
2. Look if a new version of Inkscape is available and whether our work project should cut over to build on that instead of the old version.

## Project scope

We are parents and mentors of future entrepreneurs and we see every day how fruit stands teach basic business skills and customer service to the next generation.

This My Fruit Stand kit includes everything we've learned for a minimal fruit stand, with careful attention to minimize build requirements and make the project suitable for a wide variety of people.

We specifically will not adopt any changes that require power tools for building your fruit stand.

> [!NOTE]
> In the first paragraph, briefly introduce your community, who they are and why they care.
>
> After that, add your project's scope. This tells people what kinds of things you care about. This inspires people to become *contributors* here when they are doing their own work and see that their work is also welcome here.
>
> Last, it is good to also say what is out-of-scope. These exclusions serve the same purpose and demonstrate that you are thoughtful about your scoping.

## References

1. We use "Title Case" only for proper nouns, this includes the name of our project. We have a separate style guide for other word choice and typography decisions we have settled on.
1. This project is built based on [best practices documented in project-template](https://github.com/fulldecent/project-template), release v1.3.0.
1. This project is released under the [MIT license](./LICENSE.md).

> [!NOTE]
> We use an MIT license for this template. You should carefully consider which license to apply to your own project. Replace the copyright line in LICENSE.md.
>
> We cite a non-existent style guide here. You may add one or add your own rules, to achieve a consistent voice even with diverse contributors.
>
> If your project materially relied on external sources to make some decisions, cite them here.
