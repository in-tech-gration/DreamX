# Dream X

  ![](./assets/header.png)

## DETAILS

  - Based on `Jekyll` (requires `Ruby`)
  - Based on [`GitHub Pages`](https://pages.github.com/)

## REQUIREMENTS

  - [**Ruby**](https://www.ruby-lang.org/en/) installed
    - Check if `ruby` is installed on your system via `ruby -v`
  - [**Nodejs**](https://nodejs.org/en) installed 
    - Check if `nodejs` is installed on your system via `node -v`
  - [**Syllabus Generator (sgen)**](https://github.com/in-tech-gration/sgen)

## HOW CREATE A NEW X PLATFORM

  - Create directory: `mkdir MLX`
  - Change to the directory: `cd MLX`
  - Copy the `.gitignore` file found in this repository to the newly created directory
  - Initialize the directory as a `git` repository
    - `git init`
  - Initialize the directory as a `nodejs` project:
    - `npm init -y`
  - Add the following entries to the `scripts` section of the `package.json`:

  ```json
  "scripts": {
    "build:jekyll": "bundle exec jekyll _3.9.3_ build --incremental --config _offline.yml",
    "serve:jekyll": "bundle exec jekyll _3.9.3_ serve --incremental --config _offline.yml"
  },
  ```

  - Copy the `Gemfile` found in this repository or create the file and add the following:
    - `touch Gemfile`
  
  ```Gemfile
  source "https://rubygems.org"

  # https://github.com/github/pages-gem
  gem 'github-pages', group: :jekyll_plugins
  gem "webrick", "~> 1.8"
  ```

  - Create a `README.yaml` file that includes the properties `input` and `output` which define a Markdown file used as a template and the output filename respectively.
  
  ```yaml
  input: README.draft.md
  output: index.md
  ```

  - Create the `README.draft.md`
  - Run the `sgen README.yaml` command that will produce the `index.md` given the `README.draft.md` template.

## TODO

- [ ] Convert this repository to a GitHub Template