# Lone Rock Point Developer Playbook

[Repo](https://github.com/Lone-Rock-Point/Lone-Rock-Point.github.io) | [Site](https://lone-rock-point.github.io/)

## Project Summary

This is the Lone Rock Point Developer Playbook. The purpose is to document the way we do work. It is not meant to be final, rather it should be continuously updated.

## Architecture

This project uses [github pages](https://pages.github.com) - githubs static page "hosting" option. These pages are built with [Jekyll](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll) using markdown. 

## Contributing

Jekyll takes markdown files and mixes it with a theme to generate static html. To update content in this repo you need to update the appropriate `.markdown` file.

`index.markdown` functions as a table of contents and contains tables with links to other markdown files. Most other markdown files will contain headings. These become IDs when Jekyll is run. 

Example: this `[Namespaces](code#namespaces)` becomes a link to the code markdown file at the `namespaces` heading. 

YOU ONLY NEED TO CHANGE MARKDOWN FILES, GITHUB WILL HANDLE THE BUILD AND EJECT THE NEW STATIC FILES FOR YOU.

## Building

You only need to run a build if you are trying to see how your changes appear before merge.

Because this is Jekyll it runs on ruby. I have found local ruby tooling to be difficult so I prefer to work on this project in github codespaces. You are welcome to set up your local dependencies to make the following work.

In Codespaces: 
* Open the terminal and run `bundle install`
* Run the command `jekyll serve`
* Codespaces will pop up a modal linking you to a testing build.
* Make changes to markdown files.
* Reload the test build to confirm the changes are what you expected.
