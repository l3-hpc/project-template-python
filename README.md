# Template for creating a Notebook with Python 

This is a template for creating a Jupyter Notebook in Python, originally created for NOAA RESTORE's:

**Oysters, Blue Crabs, and Spotted Seatrout:** ***Building Resilience to Environmental Trends and Variability in the Gulf of Mexico***

Using GitHub and Binder, share your work:
- Describe your project
- Add Lat/Lon information to make an interactive map of the study area and for station data
- Do plots and analysis

In this Notebook, we create an interactive map of station data, plot a time-series of temperature and salinity for a sample station, then download data and make plots for additional stations.

Click on the Binder button to open the Notebook:
[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/OyBcSt/project-template-python/HEAD?labpath=index.ipynb)

This example repo uses Python.  ([Using R? Check Here.](https://github.com/OyBcSt/project-template-r))

# Instructions

## Create a new repo from template
Starting from the landing page of this repo, click the green button **Use this template** then choose **Create a new respository**.

Choose the Owner
- If your project is NOAA RESTORE, please change **Owner** to **OyBcSt**.  
- If you don't see OyBcSt as an option, [Contact Lisa](mailto:lllowe@ncsu.edu) to be added as a collaborator.  

Choose the Repository name
- Choose something that indicates the *type* of project, e.g., hydro, climate, fisheries, etc.

## Modify the contents

README, scripts, and plain text files can be edited directly from GitHub by clicking the pencil icon, then click the green **Commit changes** button at the bottom of the page.

Change the README:
- Go to ***README.md***.  Click the pencil, and edit it directly to describe your project.
- Change the address for the Binder button...remember, the button is pointing at the *template*.  See below.
- [For Reference: GitHub markdown syntax](https://docs.github.com/en/github/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)

How to get the Binder button code:
- Go to https://mybinder.org (in a new tab).
- Paste the URL to *your new repo*.
- Put ***index.ipynb*** in the box for File.
- Where it says **Expand to see...**, click and copy the Binder button code.

Test the Binder button:
- Click the modified Binder button, and verify a working Notebook is being launched from *your new repo*.

The first time you launch the Binder, it may take a long time.  Binder has to build an image with your new environment.  [More on Binder](https://the-turing-way.netlify.app/communication/binder/zero-to-binder.html)

## Modify the Notebook

Edits to the Notebook while in Binder are not saved to GitHub.  When modifying the Notebook in Binder, periodically **Save Notebook**, then **Download** the file locally.  Then the local files must be added back to GitHub.

### No *git* for me please!
To add local files back to the repo, go to the GitHub page, click **Add file**, then **Upload files**.

### A bit of *git*
If you do lots of changes, **Upload files** will get old fast. 

Personally, I clone the repo locally, from Mac terminal:
```
git clone [https://address/reponame]
cd reponame
```

Then, I modify things while in Binder, **Save Notebook**, **Download**, and I download to **reponame**.  Then, from Mac terminal, I do
```
git status
```
Check the status.  The index.ipynb is probably the only thing that changed.  And if it *should* have changed but *didn't*, you might want to `Save` and `Download` again.  Check the download path.  Then:
```
- git add .
- git status
- git commit -m "added more notebook"
- git push
```

If you were modifying the ***README.md*** online, you will need to pull those in before pushing out your changes:
```
- git pull
```

For Windows users, I recommend MobaXterm for command line tasks. [Video tutorial: Using MobaXterm](https://youtu.be/ycUBjqyjORE)

**Contact me if you need help with git**.  We can develop some training and documentation based on what folks are having problems with.


## Do I have to use Binder to develop the Notebook?

If your Notebook is published and established, I think it is safer to modify things *within Binder* so you don't accidentally break your environment.  

If you are developing a *new* Notebook, or need to make substantial changes, then I suggest...

For beginners:
- Install [Anaconda](https://www.anaconda.com)
- Open Anaconda, Launch Jupyter Notebook
- Find index.ipynb, or create a new file, modify, and save.
When the Notebook is ready, use `git` as above to push changes.  Note: you can have several Notebooks in one GitHub repo.  

Binder has to build your environment.  If new libraries are needed for script modifications, you may need to change the runtime, or install new packages.  That is what this file does
- environment.yml

For Not Beginners:
- It is better to install miniconda, create a yaml file with dependencies, then `conda env create`, for each project.  
- [See this for more about Conda](https://hpc.ncsu.edu/Software/Apps.php?app=Conda)

**Contact me if you need help with the environment.** We can develop some extra documentation based on what folks are having problems with.


# Thank you NOAA and NSF!
*This work was funded by National Oceanic and Atmospheric Administration's RESTORE Science Program under award NA19NOS4510194. The modeling data is being hosted on Open Storage Network (OSN), through allocation EES210015 from the Advanced Cyberinfrastructure Coordination Ecosystem: Services & Support, which is supported by National Science Foundation grants #2138259, #2138286, #2138307, #2137603, and #2138296.*
