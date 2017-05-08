# Mkdocs quickstart guide 
This guide is meant to explain the setup of this project skeleton and the use of the AI2 mkdocs theme. You should refer 
to [the official mkdocs documentation](http://www.mkdocs.org) for more detail.
## Installation
Mkdocs is pip-installable:
```python
pip install mkdocs
```
## Configuration 
Here is a simple example config file for a mkdocs site:

```yaml
site_name: Generic Data explorer  # The site name will appear prominently on a site's homepage, and should reflect the dataset. 
theme: null  # If using a locally defined theme this will be set to null (or left out). The theme name if using a stock theme
theme_dir: './material_ai2_mkdoc'  # Path to the theme directory being used.
repo_url: 'https://github.com/allenai/<your repo>'   # Link to project repo, if applicable.
repo_name: '<Your Repo Name>'  # The repo name that'll be displayed.
download_url: '<Your Download URL>'  # Download link to the dataset.
extra:  # Extra parameters used by a theme.
  font:  # Custom font setting.
    text: Oxygen
    code: Oxygen

pages: @   # Define site structure without hierarchy
    - home: index.md  # Home page
    # The pages below will be specific to a dataset
    # these are defined as  <page name to display>: <markdown file in the the docs directory the page will be generated from. 
    - dataset structure: structure.md  # Ideally a description of the formatting of the dataset should be provided   
    - datapoint 1 : datapoint_1.md  # A page for single portion of your dataset (the size/level of detail will depend on the dataset) 
```

## AI2 Theme
The AI2 theme is packaged with this example and is set as shown in the config file above. If you need any modifications 
to mkdocs behaviour, it's best to set these at the theme level if possible. As an example, if your dataset is too large
for the standard search function to work effectively, this can be remedied by a change in the theme's behaviour.

## Adding documents
The 

## Build
Building is done simply
```bash
mkdocs build
```

## Local Development
While building a dataset page, the work in progress can be previewed by running:
```bash
mkdocs serve 
```
This will launch a local server and rebuild the site whenever any changes are detected to the project.

## Deploy
After building, the completed site can be deployed to AWS by... TODO

## Setting DNS redirect
TODO...
