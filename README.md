[![Website](https://github.com/carpentries/workshop-template/actions/workflows/website.yml/badge.svg)](https://github.com/carpentries/workshop-template/actions/workflows/website.yml)

# The Carpentries Workshop Template

This repository is for UCSB Carpentry R Geospatial (April 7, 2022), using The Carpentries' ([Software Carpentry][swc-site], [Data Carpentry][dc-site], and
[Library Carpentry][lc-site]'s) template for creating websites for workshops. Steps that have been completed are striked through.

2. Please *do your work directly in the repository's `gh-pages` branch*, since that is what is
   [automatically published as a website by GitHub][github-project-pages].


## Creating a Repository

~~1.  Log in to GitHub.
    (If you do not have an account, you can quickly create one for free.)
    You must be logged in for the remaining steps to work.~~

~~2.  On this page (<https://github.com/carpentries/workshop-template>),
    click on the green "Use this template" button (top right)~~

    ![screenshot of this repository's GitHub page with an arrow pointing to the the 'use this template' button on the top left](fig/select-github-use-template.png?raw=true)

~~3.  Select the owner for your new repository.
    (This will probably be you, but may instead be an organization you belong to.)~~

~~4.  Choose a name for your workshop website repository.
    This name should have the form `YYYY-MM-DD-site`,
    e.g., `2016-12-01-oomza`,
    where `YYYY-MM-DD` is the start date of the workshop.
    If your workshop is held online, then the respository name should have `-online` in the end.
    e.g., `2016-12-01-oomza-online`~~

~~5.  Make sure the repository is public, leave "Include all branches" unchecked, and click
on "Create repository from template".
You will be redirected to your new copy of the workshop template respository.~~

~~6. Your new website will be rendered at `https://your_username.github.io/YYYY-MM-DD-site`.
For example, if your username is `gvwilson`, the website's URL will be
`https://gvwilson.github.io/2016-12-01-oomza`.~~

If you experience a problem, please [get in touch](#getting-and-giving-help).

## Customizing Your Website (Required Steps)

There are two ways of customizing your website. You can either:

- edit the files directly in GitHub using your web browser
- clone the repository on your computer and update the files locally

### Updating the files on GitHub in your web browser

~~1.  Go into your newly-created repository,
    which will be at `https://github.com/your_username/YYYY-MM-DD-site`.
    For example,
    if your username is `gvwilson`,
    the repository's URL will be `https://github.com/gvwilson/2016-12-01-oomza`.~~

~~3.  Ensure you are on the gh-pages branch by clicking on the branch under the drop
    down in the menu bar (see the note below):~~

    ![screenshot of this repository's GitHub page showing the "Branch" dropdown menu expanded with the "gh-pages" branch selected](fig/select-gh-pages-branch.png?raw=true)

~~3.  Edit the header of `index.md` to customize the list of instructors,
    workshop venue, etc.
    You can do this in the browser by clicking on it in the file view on GitHub
    and then selecting the pencil icon in the menu bar:~~

    ![screenshot of top menu bar for GitHub's file interface with the edit icon highlighted in the top right](fig/edit-index-file-menu-bar.png?raw=true)

    Editing hints are embedded in `index.md`,
    and full instructions are in [the customization instructions][customization].

~~4.  Remove the notice about using the workshop template in the `index.md` file. You can safely
    delete everything between the `{% comment %}` and `{% endcomment %}` (included) as indicated
    below (about from line 35 to line 51):~~

    ```jekyll
    {% comment %} <------------ remove from this line
    8< ============= For a workshop delete from here =============
    For a workshop please delete the following block until the next dashed-line
    {% endcomment %}

    <div class="alert alert-danger">
      ....
    </div>

    {% comment %}
     8< ============================= until here ==================
    {% endcomment %} <--------- until this line
    ```

~~4.  Edit `_config.yml` to customize certain site-wide variables, such as: `carpentry` (to tell your
    participants the lesson program for your workshop), `curriculum` and `flavor` for the
    curriculum  taught in your workshop, and `title` (overall title for all pages).~~

    Editing hints are embedded in `_config.yml`,
    and full instructions are in [the customization instructions][customization].

*** this needs to be done!!!
5. Edit the `schedule.html` file to edit the schedule for your upcoming workshop. This file is
   located in the `_includes` directory, make sure to choose the one from the appropriate `dc` (Data
   Carpentry workshop), `lc` (Library Carpentry), or `swc` (Software Carpentry) subdirectory.

## Optional but Recommended Steps


### Update your repository description and link your website

~~At the top of your repository on GitHub you'll see~~

~~~
No description, website, or topics provided. — Edit
~~~

~~Click 'Edit' and add:~~

~~1.  A very brief description of your workshop in the "Description" box (e.g., "Oomza University workshop, Dec. 2016")~~

~~2.  The URL for your workshop in the "Website" box (e.g., `https://gvwilson.github.io/2016-12-01-oomza`)~~

~~This will help people find your website if they come to your repository's home page.~~


## Additional Notes

**Note:**
please do all of your work in your repository's `gh-pages` branch,
since [GitHub automatically publishes that as a website][github-project-pages].

**Note:**
this template includes some files and directories that most workshops do not need,
but which provide a standard place to put extra content if desired.
See the [design notes][design] for more information about these.

Further instructions are available in [the customization instructions][customization].
This [FAQ][faq] includes a few extra tips (additions are always welcome)
and these notes on [the background and design][design] of this template may help as well.


## Creating Extra Pages

In rare cases,
you may want to add extra pages to your workshop website.
You can do this by putting either Markdown or HTML pages in the website's root directory
and styling them according to the instructions give in
[the lesson template][lesson-example].

There ARE extras for this lesson. How do we light them up?


## Installing Software

If you want to set up Jekyll so that you can preview changes on your own machine before pushing them
to GitHub, you must install the software described in the lesson example [setup
instructions](https://carpentries.github.io/lesson-example/setup.html#jekyll-setup-for-lesson-development).

## Setting Up a Separate Repository for Learners

If you are teaching Git,
you should create a separate repository for learners to use in that lesson.
You should not have them use the workshop website repository because:

* your workshop website repository contains many files that most learners don't need to see during
  the lesson, and

* you probably don't want to accidentally merge a damaging pull request from a novice Git user into
  your workshop's website while you are using it to teach.

You can call this repository whatever you like, and add whatever content you need to it.

## Getting and Giving Help

We are committed to offering a pleasant setup experience for our learners and organizers.
If you find bugs in our instructions,
or would like to suggest improvements,
please [file an issue][issues]
or [mail us][email].

[email]: mailto:team@carpentries.org
[customization]: https://carpentries.github.io/workshop-template/customization/index.html
[dc-site]: https://datacarpentry.org
[design]: https://carpentries.github.io/workshop-template/design/index.html
[faq]: https://carpentries.github.io/workshop-template/faq/index.html
[github-project-pages]: https://help.github.com/en/github/working-with-github-pages/creating-a-github-pages-site
[issues]: https://github.com/carpentries/workshop-template/issues
[lesson-example]: https://carpentries.github.io/lesson-example/
[self-organized-workshop-form]: https://amy.carpentries.org/forms/self-organised/
[swc-site]: https://software-carpentry.org
[lc-site]: https://librarycarpentry.org
