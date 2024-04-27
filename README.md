# A Template for Writing Japanese Thesis

This repository is a template for writing Japanese thesis. 
It is based on the [template](https://github.com/pddg/latex-template-ja?tab=readme-ov-file) for writing Japanese documents with LaTeX.
And it is customized for writing thesis on Dev Container.

## 🛠️ Setup

1. Open this project in VS Code.

1. (First time only) Add the extension [Remote Development](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.vscode-remote-extensionpack) Add the extension [Remote Development]().
   
1. Press the `><` icon at the bottom-left corner of VSCode and execute `Reopen in Container`.
   
1. Wait (it will take a while the first time, sometimes 15~20 minutes).

  VS Code succeeds when the files appear on theleft side of the screen and they are lined updirectly under the `WORKDIR` tab.

1. Place any TeX file under `WORKDIR`, select it and open it.

  For example, a paper template from the Information Processing Society of Japan.
  (https://www.ipsj.or.jp/journal/submit/style.html)

1. Run a suitable compilation recipe from the LaTeX Workshop extension.
   
  (Compilation is automatically executed when you open and save a TeX file.)

1. If the compilation is successful, a PDF file will be generated in the `out` directory.

  You can also open the generated PDF by clicking the preview icon 🔍 in the upper right corner of the opened tex file.

## Recommended Writing Procedures

0. initialize Git management

  ```sh
  git init
  git add .
  git commit -m "initial commit"
  ````

1. put a directory on `WORKDIR` containing TeX, style files, etc.

1. Open and edit any tex file. Open any tex file, edit it, and save it. Commit as needed.

1. Submit the compiled PDF file to your advisor. Have it proofread.

  Tag the file when you submit it.

  ```sh
  git tag -a v1.0 -m "first submission"
  ````

1. If you need to resubmit, correct the mistakes and sae the file.
  
  Select the Extensions tab > LaTeX Workshop > Build LaTeX project > Recipe: mkDiffTAG.

  A diff file (XXX-diffv◯.tex) with the latest v◯ tag is generated.

1. When the diff file is compiled, a PDF file with the edited part in red is compiled.

  Return to 4.

> The scripts related to latexdiff-vc are in the .bin file.
>
> You can diff from any commit, or change the format of tags as you wish.

## 🏁 How to finish work

When you finish, "terminate the connection" from the `><` icon of VSCode

## ? If compilation does not work

- Select a different build recipe from the Latex Workshop extension.

  Recipes can also be added or modified by editing `.vscode/settings.json`.

  When a recipe is added, it will be added to the Build LaTeX project section of the LaTeX Workshop, and the build will run when you select it.

---

## Feature

- Build tex source without LaTeX setup
  - Use Docker instead
- Automated build on cloud
  - GitHub Actions
  - BitBucket Pipelines

## Environment

- macOS 10.14 or later
- Ubuntu 18.04 LTS or later
- Windows 10

And Docker is required.


- Docker Desktop for Mac 2.1 or later
- Docker 18.06 or later
- Docker Desktop for Windows

This repository will use TeX Live 2021 on Ubuntu 20.04 LTS. See https://github.com/pddg/latex-docker to get more detail.

VSCode is recommended tool to edit TeX sources.

![demo](https://github.com/pddg/latex-template-ja/blob/master/figures/screenshot.png)

## License

CC0

## Author

Shoma Kokuryo
