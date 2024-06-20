
# Academic Pages

![pages-build-deployment](https://github.com/academicpages/academicpages.github.io/actions/workflows/pages/pages-build-deployment/badge.svg)

Academic Pages is a Github Pages template for academic websites.


# Getting Started

1. Register a GitHub account if you don't have one and confirm your e-mail (required!)
1. Click the "Use this template" button in the top right.
1. On the "New repository" page, enter your repository name as "[your GitHub username].github.io", which will also be your website's URL.
1. Set site-wide configuration and add your content.
1. Upload any files (like PDFs, .zip files, etc.) to the `files/` directory. They will appear at https://[your GitHub username].github.io/files/example.pdf.  
1. Check status by going to the repository settings, in the "GitHub pages" section
1. (Optional) Use the Jupyter notebooks or python scripts in the `markdown_generator` folder to generate markdown files for publications and talks from a TSV file.

See more info at https://academicpages.github.io/

# Running Locally

If you are using a **Windows** computer, I recommend to use Windows Subsystem for Linux (WSL) and access files with Visual Studio Code. [how to?](https://learn.microsoft.com/en-us/windows/wsl/install)

1. Log in WSL and run `sudo apt-get update` to refresh your library list.
2. Install dependencies: `sudo apt-get install build-essential`.
3. Clone and `cd` the repository.
4. Make sure you have ruby-dev, bundler, and nodejs installed: `sudo apt install ruby-dev ruby-bundler nodejs`
5. Run `bundle install` to install ruby dependencies. If you get errors, delete Gemfile.lock and try again.
6. Run `jekyll serve -l -H localhost` to generate the HTML and serve it from `localhost:4000` the local server will automatically rebuild and refresh the pages on change. If it doesn't work, add `--force_polling` to this command.

For **MacOS** computers, the OS has preinstalled `ruby` with a version of 2.6 (checked at 06/20/2024). You can check it by running `which ruby` and `ruby -v`. It is better to build a local `ruby` environment. Here are two links that introduce how to use `homebrew` to install and manage `ruby`. [Link 1](https://mac.install.guide/ruby/12) and [Link 2](https://jekyllrb.com/docs/installation/macos/). 

1. Follow the above links to install `ruby`.
2. `brew install node` to install `nodejs`.
3. `gem install bundler`
4. `cd ${Your Cloned Project Path}` and run `bundle install`. This command will install ruby dependencies based on `Gemfile`. If you get errors, delete Gemfile.lock and try again.
5. Run `jekyll serve -l -H localhost` to generate the HTML and serve it from `localhost:4000` the local server will automatically rebuild and refresh the pages on change.

# Maintenance 

Bug reports and feature requests to the template  should be [submitted via GitHub](https://github.com/academicpages/academicpages.github.io/issues/new/choose). For questions concerning how to style the template, please feel free to start a [new discussion on GitHub](https://github.com/academicpages/academicpages.github.io/discussions).

This repository was forked (then detached) by [Stuart Geiger](https://github.com/staeiou) from the [Minimal Mistakes Jekyll Theme](https://mmistakes.github.io/minimal-mistakes/), which is © 2016 Michael Rose and released under the MIT License (see LICENSE.md). It is currently being maintained by [Robert Zupko](https://github.com/rjzupkoii) and additional maintainers would be welcomed.

## Bugfixes and enhancements

If you have bugfixes and enhancements that you would like to submit as a pull request, you will need to [fork](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/working-with-forks/fork-a-repo) this repository as opposed to using it as a template. This will also allow you to [synchronize your copy](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/working-with-forks/syncing-a-fork) of template to your fork as well.

Unfortunately, one logistical issue with a template theme like Academic Pages that makes it a little tricky to get bug fixes and updates to the core theme. If you use this template and customize it, you will probably get merge conflicts if you attempt to synchronize. If you want to save your various .yml configuration files and markdown files, you can delete the repository and fork it again. Or you can manually patch.
