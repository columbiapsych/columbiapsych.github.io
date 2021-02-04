# Welcome

This repository contains the code for the Columbia Psychology Prospective Students' Day website.

**If you are a student looking for the website, please visit https://columbiapsych.github.io.

## RStudio Instructions for Developers

- If this is your first time working on this website, after being added as a collaborator (ask Emily or Camille!), copy the repository link here. Then, open RStudio and click **File** > **New Project...**. In the dialog box that pops up, select **Version Control**, then **Git**, and then paste the name of the repository into the **Repository URL:** field. Then click the **Create Project** button.

- You'll see that this repository contains two branches:

    * The `main` branch contains all of the code for the site. Any site edits should be made here.
    * The `gh-pages` branch contains a copy of the `public` folder from the main branch. You should never directly edit this branch!

- To edit the site:

    * First, open RStudio on your computer by opening the R project file (`columbiapsych.github.io.Rproj`).
    * Make sure you are in the `main` branch. If you are in `gh-pages`, switch to the `main` branch before working!
    * In RStudio, click the blue "Pull" arrow on the **Git** tab to ensure your computer has the latest versions of the website files from the remote Github repository.
    * Make your changes to the code in the `main` branch. As you are working, feel free to run the line `blogdown::serve_site()` to see a rendered version of the site with your changes.
    * Once you have completed your changes, run `blogdown::serve_site()` once more to make sure that all of your revisions have been incorporated and rendered.
    * Then, commit these changes within the **Git** tab, and click the green "Push" arrow to push them to the remote Github repository.
    * Finally, you will run a line of code that automatically pushes your revisions from `main\public` to `gh-pages`. (In case you're curious: The repository is structured in this way because Github Pages needs the final, rendered site files to be in the top level of the branch, and our `blogdown` site can only publish these final, rendered site files into a subfolder.) The only way to do this is in the command line (the "shell"). To do so, click the blue gear icon within the **Git** tab, and click **Shell...**. Within the command line prompt that opens, run the following line of code: `git subtree push --prefix public origin gh-pages`.
    * Your changes should now have been pushed live! Check them out at https://columbiapsych.github.io to be sure.