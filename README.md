# About this repository [![Build Status](https://travis-ci.org/psadmin-io/psadmin-wiki.svg?branch=master)](https://travis-ci.org/psadmin-io/psadmin-wiki)

This is the GitHub repo for the psadmin.io Community Wiki (<http://wiki.psadmin.io>). The Community Wiki is a place for PeopleSoft Administrators to share documentation on setting up new features, how they resolved issues, and anything else they would like to share.

## How to contribute

Any one can contribute to the Communtiy Wiki. To make a contribution or edit, you'll need Git installed. It's also recommended you use a good text editor (like SublimeText, VS Code, Notepad++, vi) and are familiar with [Markdown formatting](https://guides.github.com/features/mastering-markdown/). 

### Clone the wiki git repository

To add your change, use Git to clone this repository to your local machine:

    git clone https://github.com/psadmin-io/psadmin-wiki.git

This will copy the repositiory to the folder `psadmin-wiki`. 

### Create a new branch

Next, open the repository and create a new branch:

    cd psadmin-wiki
    git checkout -b [new-branch-name]

For your branch name, use something descriptive so people know what the branch contains. (E.g, `update-README`, `push-notification-install`, etc)

### Add your article

All the wiki articles live under the `user` folder, and are organized into a few sections. Put your file under the section that most applies to the topic you are contributing. Under each section is an OVERVIEW articles with guidelines on what the topics are included.

* PeopleTools
* Database
* Middleware
* PeopleSoft Cloud Architecture
* Server Administration
* Development

Now you can use your text editor to add a new article. For example, we'll add a new article that shows a sample `psft_customizations.yaml` file under the *PeopleSoft Cloud Architecure" section. I'll create a new file with VS Code:

     code user/pca/sample_yaml.md

#### Front-data

At the top of every wiki article is some YAML data that tells the wiki how to render the document.

    ---
    title: Sample psft_customizations.yaml
    layout: en
    permalink: /user/pca/sample_yaml/
    ---

Update the title and permalink values. For the `permalink`value, use the convention `/user/<section>/<filename>/` The permalink will be the URL to the wiki page.

#### Wiki article

Start the wiki article with a heading (two `##`) and the title. Everything after here is the article. You can use Markdown formatting throughout the article to create code blocks, headings, lists, etc.

    ## Sample psft_customizations.yaml File

    Below is a sample `psft_customizations.yaml` file to give you an idea of how to define configuration for the DPK.

#### Gists

You can include Github gists if you want. Copy the code below and replace the `src=` with the link to your Gist.

    <script src="https://gist.github.com/iversond/0c096258ffe2d624d1c64b8aaffad846.js"> </script>




## How to check your edit before sending PR

You can inspect how your edits will be reflected by the documentation site.

### Install dependencies

1. Make sure you have Ruby and RubyGems installed.

1. Install [bundler](http://bundler.io/):

    ```sh-session
    $ gem install bundler
    ```

1. Install application dependencies:

    ```sh-session
    $ bundle install --binstubs
    ```

### Generate documentation

Run

```sh-session
$ ./bin/jekyll build
```


### Run application server

You are now ready to start your documentation site, using Jekyll or Puma.
For documentation edits, Jekyll is sufficient.

#### Starting and inspecting edits with Jekyll

1. Run Jekyll server:

    ```sh-session
    $ ./bin/jekyll serve
    ```

1. Open [localhost:4000](http://localhost:4000/) in your browser.

