# stat999-myst

This repository contains a MyST-based template for class website. You can see a preview of it at [https://berkeley-scf.github.io/stat999-myst](https://berkeley-scf.github.io/stat999-myst). This template is intended to be forked and altered for other courses.

## MyST Template Capabilities

- Create a website by modifying content in a GitHub repository.
- Create documents from markdown files or Jupyter notebooks.
- Include LaTeX and LaTeX macros for mathematical notation.
- Embed external webpages (such as Google calendars) as iframes within a page.
- Render documents as HTML or PDF (the latter for documents that students will download).
- MyST Markdown includes various nice features such as automatic navigation links, callouts, tables, images, code blocks, diagrams, etc.


## Terminology

- "Rendering" a document or a site involves converting the *source* markdown or notebook files to html.
- "Previewing" a site involves rendering the site and displaying it locally on your computer (i.e., at `localhost:<port>` in a web browser.
- "Publishing" a site involves pushing the rendered site to the `gh-pages` branch of the GitHub repository so it can be viewed at the public URL.

## Instructions [UNDER CONSTRUCTION]

These instructions have been tested under macOS.

Current problems/questions:
  - **Use this template** is only available if logged in to GitHub. Not sure if it will be available to someone else who is logged in.
  - What format should we use for class repo names for individual semesters, e.g., stat555-sp24, stat555-spring-2024, etc..
  - What github.com or github.b.e account should instructors use? Perhaps github.com/berkeley-stat or github.b.e/berkeley-stat or github.b.e/statistics

1. Fork this `stat999-myst` repository template:

   a. Visit https://github.com/berkeley-scf/stat999-myst.
   b. Above the file list click **Use this template** and then **Create a new repository**. This will then bring you to a screen where you'll configure your new repository.
   c. Do not enable the **Include all branches** checkbox.
   d. Choose your repository name to follow the pattern, `stat-NUMBER-TERM`, e.g.`stat-555-fa23` [TBD]
   e. You might choose the default of having your repository be public or choose that it be private while you are setting things up. Or you might choose for it always to be private.
   f. Click on **Create Repository**.

2. Clone your newly created repository into a local working directory on your computer. For the purposes of these instructions, we'll pretend your repository is at https://github.com/example/stat555-myst.
   - You can do this from the terminal/commandline or within a Git graphical application (e.g., `GitHub Desktop`).
   - From the terminal it would look like this:
     ```bash
     git clone https://github.com/example/stat555
     cd stat555
     ```

3. This workflow needs some command-line programs such as `nodejs` and [myst](https://mystmd.org/guide/quickstart). We recommend you install a Conda distribution, such as [Miniforge](https://github.com/conda-forge/miniforge) or [Anaconda](https://www.anaconda.com/download#downloads). We have provided an `environment.yml` file so that you can run the commands below to install all dependencies and activate the environment. This keeps things separate from any other projects you're working on:
     ```bash
     # You can replace `mamba` with `conda`.
     mamba env create -f environment.yml
     
     # Now you can activate the environment.
     # You can use `mamba activate` or `conda activate`,
     # but these require that you have run `mamba init` or `conda init`,
     # which modifies your shell.
     mamba activate stat-myst-site
     
     # Alternative you can activate like this, without
     # having do the `init` step mentioned above.
     source activate stat-myst-site
     ```

   Whenever you need to start up a new terminal to work on your website, first activate the the environment that contains the necessary programs with `mamba activate stat-myst-site`. Otherwise your terminal may report that it cannot find `myst` or its dependencies.


4. Begin making changes relevant to your course.
   - Modify the site's metadata in `myst.yml`. Notable fields include the course title, description, author, and github URL. You can also edit links to external resources for your course, such as bCourses and Ed.
   - Modify the table of contents in `_toc.yml` to reflect the structure you want.
   - Update `README.md` to remove all the instructions we provide (i.e., this text you are reading!).
   - Edit the other markdown files in the working directory and add new markdown or notebook files as desired.
   - Update `index.md` to reflect the material you want displayed in the main page.
   - You can make use of various MyST features discussed in the [MyST Guide](https://mystmd.org/guide).

5. Run `myst init` in the working directory to initialize your working directory. When prompted, let the command run `myst start` for you to generate a preview. `myst` will display a localhost URL where the site preview is running, such as http://localhost:3000. Open this URL in your browser.

   **Note:** When `myst` detects problems in the markdown that prevent the website from rendering correctly, it will print the file and line number containing the issue. If this happens, fix the file and rerun `myst init`.

   **Note:** If you are on a Mac, `myst` may prompt you to allow `node` to accept incoming network connection. Allow this to enable website previewing to work.

   You can leave `myst` running as you make changes to the source files; saving changes to the source files will generally will be reflected live in your browser, though you may sometimes need to navigate away and back or reload the page.

   You can also run `myst build` to create the static HTML (in the `_build` directory) without automatically displaying it.

   **Note:** Do not commit the files in `_build` to your repository as they will be frequently regenerated and having them in the repository can complicate matters.

6. Update your repository with the changes to your source files. First tell git about all files that should be in your repo.

   ```bash
   git add NEWFILE1.md NEWFILE2.md NEWDIRECTORY
   ```

   Then commit your changes and push to github:
   ```bash
   git commit -m "Initial checkin for Stat 555."
   git push
   ```

    If you modify an existing file, you can either do `git add currentfile.md` or include the `-a` flag when you run `git commit` to automatically update files that Git is already keeping track of, e.g., after modifying unit 7 files, `git commit -am "Updated Unit 7"`.


7. Enable Github to host your website with GitHub Pages. You can Control-C to stop the running `myst init`, then run:

   ```bash
   myst init --gh-pages
   ```
   Follow the directions as prompted.

8. As you make changes to your pages and push to GitHub, it will rebuild your site. You can observe this build process at github by clicking on the Actions button at the top of your repository. It usually takes a couple of minutes for this to complete. If there are no problems, your website will be publicly available at https://{your_github_id}.github.io/{your_github_repo}. For example if your repository is at https://github.com/example/stat555, your website will be at https://example.github.io/stat555/.

9. We will work with you to give your website a friendly URL in a department-standardized format, such as https://stat555.berkeley.edu. Just let us know when your website is ready.

The SCF is happy to help. Please [contact us](https://statistics.berkeley.edu/computing/how-get-help) if you are a Berkeley Statistics instructor and you run into problems or questions.
