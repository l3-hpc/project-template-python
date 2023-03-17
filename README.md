# Template for creating a Notebook with Python 

This is a template for creating a Jupyter Notebook in Python, created for NOAA RESTORE's:

**Oysters, Blue Crabs, and Spotted Seatrout:** ***Building Resilience to Environmental Trends and Variability in the Gulf of Mexico***

Using GitHub and Binder, share your work:
- Describe your project
- Add Lat/Lon information to make an interactive map of the study area and for station data
- Do plots and analysis

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/OyBcSt/project-template-python/HEAD?labpath=index.ipynb)


This example repo uses Python.  ([Using R? Check Here.](https://github.com/OyBcSt/project-template-r))

## How to use the template to make your own repo

We're still working out the easiest way to do this, but in general:
- Starting from the [main branch of the repo](https://github.com/OyBcSt/project-template-python), click the green button `Use this template` then choose `Create a new respository`.

Choose the Owner
- If your project is NOAA RESTORE, please change 'Owner' to 'OyBcSt'.  
- That way, our work is kept together, and we don't lose your work if you leave town.  
- If you don't see OyBcSt as an option, Contact [Lisa](mailto:lllowe@ncsu.edu) to be added as a collaborator.  
- If you want to create a repo *now*, without waiting, go ahead but please let us know and we can transfer it later to OyBcSt.

Choose the Repository name
- Try to pick something that makes it easy to identify which 'type' of project, e.g., hydro, climate, fisheries, etc.

Modify the README
- Change the README.md.  Click the pencil and edit it directly to describe your project
- Change the address for the Binder button...remember, the button is pointing at the *template*.  See below.

How to get the Binder button code:
- Go to [https://mybinder.org](https://mybinder.org)
- Paste the URL to *your* new repo
- Put `index.ipynb` in the box for File
- Where it says 'Expand to see...', click and copy the binder code.

Test the Binder button:
- Click the modified Binder button, and check that you have a working Notebook that is being launched from *your new repo*.

## How to modify the repo

Here is what we need to work out, depending on how much you care to learn about GitHub, Notebooks, and Environments.

There is a lot that can be edited directly from GitHub (clicking pencils). You can work on the Notebook in Binder, but you can't save things directly back to the repo.  When modifying the notebook in Binder, you would Save Notebook, then Download the file locally.  Then you need to add it back to GitHub.

### For Folks that really don't want to learn git
If you really don't spend much time doing this, you could just go to the GitHub, click "Add file", then "Upload files" to upload the newest Notebook.

### For Folks who don't mind learning a little git, and don't do major code development in Binder
If you spend more time, that will get really annoying.  Personally, I clone the repo locally, so I have the files on my computer. Then, I modify things in Binder, Save Notebook, Download, and when I Download, I put them in the local repo.  Then, from my Mac terminal, I do
- git status
(index.ipynb is probably the only thing that changes, make sure to check)
- git add .
- git commit -m "added more notebook"
- git push

When I do this, sometimes I'm modifying the README.md online, and it will give me a warning that I need to do:
- git push

**Contact me if you need help with git**.  We can develop some training and documentation based on what folks are having problems with.

### For Folks who change the Notebook a lot, and don't want to do that in Binder
- You probably want to use Jupyter locally.  
- You can just download Anaconda and work on the Notebook, then save the new Notebooks by uploading or using git
- If you don't have scripts with complex library dependencies, Anaconda is super for making things easy for beginners.  

Binder has to build your environment.  If you add libraries to your scripts, you probably have to change the runtime, or install new packages.  That is what this file does:
- environment.yml

### For Folks in the Weeds
- If you already do development on your local machine, I strongly recommend you **do not** install Anaconda.  It changes some of the default system paths...I think it changed something really basic, like cmake.  I forget what it was, I just remember I wasn't happy. 
- If you are plagued with library dependencies, I strongly recommend you **do not** install Anaconda.  
- It is better to install miniconda, create a yaml file with dependencies, then `conda env create`, for each project.  
- [See this for more about Conda](https://hpc.ncsu.edu/Software/Apps.php?app=Conda)


**Contact me if you need help with the environment.**. We can develop some extra documentation based on what folks are having problems with.



*This work is funded by the National Oceanic and Atmospheric Administration's RESTORE Science Program under award NA19NOS4510194.*

