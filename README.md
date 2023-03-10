<!-- Improved compatibility of back to top link: See: https://github.com/othneildrew/Best-README-Template/pull/73 -->
<a name="readme-top"></a>
<!--
*** Thanks for checking out the Best-README-Template. If you have a suggestion
*** that would make this better, please fork the repo and create a pull request
*** or simply open an issue with the tag "enhancement".
*** Don't forget to give the project a star!
*** Thanks again! Now go create something AMAZING! :D
-->



<!-- PROJECT SHIELDS -->
<!--
*** I'm using markdown "reference style" links for readability.
*** Reference links are enclosed in brackets [ ] instead of parentheses ( ).
*** See the bottom of this document for the declaration of the reference variables
*** for contributors-url, forks-url, etc. This is an optional, concise syntax you may use.
*** https://www.markdownguide.org/basic-syntax/#reference-style-links
-->
[![PyPI][pypi-shield]][pypi-url]
[![Contributors][contributors-shield]][contributors-url]
[![Forks][forks-shield]][forks-url]
[![Stargazers][stars-shield]][stars-url]
[![Issues][issues-shield]][issues-url]
[![MIT License][license-shield]][license-url]
<!-- [![LinkedIn][linkedin-shield]][linkedin-url] -->



<!-- PROJECT LOGO -->
<br />
<div align="center">
  <!-- <a href="https://github.com/siemdejong/shit-happens">
    <img src="images/logo.png" alt="Logo" width="80" height="80">
  </a> -->

<h3 align="center">Customized Shit Happens</h3>

  <p align="center">
    Create your own <a href="https://boardgamegeek.com/boardgame/196379/shit-happens">Shit Happens</a> playing cards!
    <br />
    <a href="https://github.com/siemdejong/shit-happens"><strong>Explore the docs »</strong></a>
    <br />
    <br />
    <!-- <a href="https://github.com/siemdejong/shit-happens">View Demo</a>
    · -->
    <a href="https://github.com/siemdejong/shit-happens/issues">Report Bug</a>
    ·
    <a href="https://github.com/siemdejong/shit-happens/issues">Request Feature</a>
  </p>
</div>



<!-- TABLE OF CONTENTS -->
<details>
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#about-the-project">About The Project</a>
      <ul>
        <li><a href="#built-with">Built With</a></li>
      </ul>
    </li>
    <li>
      <a href="#getting-started">Getting Started</a>
      <ul>
        <li><a href="#prerequisites">Prerequisites</a></li>
        <li><a href="#installation">Installation</a></li>
      </ul>
    </li>
    <li><a href="#usage">Usage</a></li>
    <!-- <li><a href="#roadmap">Roadmap</a></li> -->
    <li><a href="#contributing">Contributing</a></li>
    <li><a href="#license">License</a></li>
    <li><a href="#contact">Contact</a></li>
    <!-- <li><a href="#acknowledgments">Acknowledgments</a></li> -->
  </ol>
</details>



<!-- ABOUT THE PROJECT -->
# About The Project

<!-- [![Product Name Screen Shot Front][<img src=product-screenshot-front width="250"/>]](https://example.com)
[![Product Name Screen Shot Back][product-screenshot-back]](https://example.com) -->
<div style="display:flex;align-items:center;">
  <div style="padding:10px;float:left;"> <img src="https://raw.githubusercontent.com/siemdejong/shit-happens/8e0a5a46b70d6a5780df125a553d25ec161fc82e/images/80-you-dont-know-how-to-use-this-tool-front.png" alt="Front." height="250"/> </div> 
  <div style="padding:10px;float:left;"> <img src="https://raw.githubusercontent.com/siemdejong/shit-happens/8e0a5a46b70d6a5780df125a553d25ec161fc82e/images/80-you-dont-know-how-to-use-this-tool-back.png" alt="Back." height="250"/> </div>  
</div>


Ever wanted to play with your own [Shit Happens](https://boardgamegeek.com/boardgame/196379/shit-happens) playing cards?
Now you can.
Write down the most miserable situations you can think of and rank them.
This project automatically outputs playing cards in pdf format.

This project is not related to the original card game.
[Open an issue](https://github.com/siemdejong/shit-happens/issues/new/choose) in case of any objections.

<!-- Here's a blank template to get started: To avoid retyping too much info. Do a search and replace with your text editor for the following: `siemdejong`, `shit-happens`, `twitter_handle`, `linkedin_username`, `email_client`, `email`, `project_title`, `project_description` -->

<p align="right">(<a href="#readme-top">back to top</a>)</p>



## Built With

[![Python][Python]][Python-url]

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- GETTING STARTED -->
# Getting Started
## Prerequisites

A virtual environment with python 3.11 or higher.

## Installation

Run
```
pip install shithappens
```
from within the target environment.

To allow for pdf merging, run `pip install shithappens[merge]`.
To show a progressbar, run `pip install shithappens[pbar]`.
To install all dependencies, run `pip install shithappens[all]`.

## Installing for developers

### Retrieve the latest version of the code
Developers should fork this repository and run
```
git clone https://github.com/<your-username>/shit-happens.git
```
This will place the sources in a directory `shit-happens` below your current working directory, set up the `origin` remote to point to your own fork, and set up the `upstream` remote to point to the `shit-happens` main repository.
Change into this directory before continuing:
```
cd shit-happens
```

### Create a dedicated environment
You should set up a dedicated environment to decouple your shithappens development from other Python and shithappens installations on your system.

The simplest way to do this is to use either Python's virtual environment venv or conda.
Here, instructions for conda are shown.
If mamba is installed, replace conda with mamba in the commands below.
```
conda env create -f environment.yml
```
Activate the environment using
```
conda activate shithappens-dev
```
Remember to activate the environment whenever you start working on shithappens.

### Installing shithappens in editable mode
Install shithappens in editable mode from the shithappens directory using the command
```
python -m pip install -e .
```
The 'editable/develop mode', builds everything and places links in your Python environment so that Python will be able to import shithappens from your development source directory.
This allows you to import your modified version of shithappens without re-installing after every change.


<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- USAGE EXAMPLES -->
# Usage

## CLI
The tool is available as a command line interface (CLI).
It requires an Excel file in the input directory (default current working directory).
The excel files must have two columns with any header.
The first column must contain the miserable situations.
The second column must contain the corresponding misery indices.
See the examples directory for an example.
```
usage: shithappens [-h] [-n NAME] [-m | --merge | --no-merge] [-s {front,back,both}] [-l {en,nl}] [-f {pdf,png}] [-r | --rank | --no-rank] [-w WORKERS] [-c CHUNKS] [input_dir]

help:
  -h, --help            show this help message and exit

input:
  input_dir             Input directory. Defaults to current working directory.

options:
  -n NAME, --name NAME  Expansion name. If no name is specified, infers name from input_dir.
  -m, --merge, --no-merge
                        Merge output. Defaults to --no-merge
  -s {front,back,both}, --side {front,back,both}
                        Side(s) to generate. Defaults to both.
  -l {en,nl}, --lang {en,nl}
                        Language. 'en' and 'nl' supported. Defaults to 'en'.
  -f {pdf,png}, --format {pdf,png}
                        Output format. 'pdf' and 'png' supported. Defaults to 'pdf'.
  -r, --rank, --no-rank
                        Rank situations and output in new file. Does not guarantee a linear ranking, i.e. situations can have equal misery index. Ignores all other options. Defaults to --no-rank.

multiprocessing:
  -w WORKERS, --workers WORKERS
                        Number of workers. Defaults to 4.
  -c CHUNKS, --chunks CHUNKS
                        Number of chunks for the workers to process. Defaults to 30.
```
The input directory must be structured as follows:
```
expansion
├───images
│   └───expansion-logo.*
├───outputs
│   ├───back
│   └───front
└───*.xlsx
```
If the output folder does not exist, it will be created.
The format of the expansion logo must be on [this list](https://pillow.readthedocs.io/en/stable/handbook/image-file-formats.html).

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- ROADMAP -->
<!-- ## Roadmap

- [ ] Feature 1
- [ ] Feature 2
- [ ] Feature 3
    - [ ] Nested Feature

See the [open issues](https://github.com/siemdejong/shit-happens/issues) for a full list of proposed features (and known issues).

<p align="right">(<a href="#readme-top">back to top</a>)</p> -->



<!-- CONTRIBUTING -->
# Contributing

Any contributions you make are greatly appreciated.

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- LICENSE -->
# License

Distributed under the GPL-3.0 license. See `LICENSE` for more information.

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- CONTACT -->
# Contact

Project Link: [https://github.com/siemdejong/shit-happens](https://github.com/siemdejong/shit-happens)

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- ACKNOWLEDGMENTS -->
<!-- ## Acknowledgments

* []()
* []()
* []()

<p align="right">(<a href="#readme-top">back to top</a>)</p> -->



<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
[pypi-shield]: https://img.shields.io/pypi/v/shithappens?color=blue&logoColor=yellow&style=for-the-badge
[pypi-url]: https://pypi.org/project/shithappens/
[contributors-shield]: https://img.shields.io/github/contributors/siemdejong/shit-happens.svg?style=for-the-badge
[contributors-url]: https://github.com/siemdejong/shit-happens/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/siemdejong/shit-happens.svg?style=for-the-badge
[forks-url]: https://github.com/siemdejong/shit-happens/network/members
[stars-shield]: https://img.shields.io/github/stars/siemdejong/shit-happens.svg?style=for-the-badge
[stars-url]: https://github.com/siemdejong/shit-happens/stargazers
[issues-shield]: https://img.shields.io/github/issues/siemdejong/shit-happens.svg?style=for-the-badge
[issues-url]: https://github.com/siemdejong/shit-happens/issues
[license-shield]: https://img.shields.io/github/license/siemdejong/shit-happens.svg?style=for-the-badge
[license-url]: https://github.com/siemdejong/shit-happens/blob/master/LICENSE
[linkedin-shield]: https://img.shields.io/badge/-LinkedIn-black.svg?style=for-the-badge&logo=linkedin&colorB=555
[linkedin-url]: https://linkedin.com/in/linkedin_username
[product-screenshot-front]: images\80-you-dont-know-how-to-use-this-tool-front.png
[product-screenshot-back]: images\80-you-dont-know-how-to-use-this-tool-back.png
[Python]: https://img.shields.io/badge/python-3776AB?style=for-the-badge&logo=python&logoColor=white
[Python-url]: https://python.org/
[React.js]: https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB
[React-url]: https://reactjs.org/
[Vue.js]: https://img.shields.io/badge/Vue.js-35495E?style=for-the-badge&logo=vuedotjs&logoColor=4FC08D
[Vue-url]: https://vuejs.org/
[Angular.io]: https://img.shields.io/badge/Angular-DD0031?style=for-the-badge&logo=angular&logoColor=white
[Angular-url]: https://angular.io/
[Svelte.dev]: https://img.shields.io/badge/Svelte-4A4A55?style=for-the-badge&logo=svelte&logoColor=FF3E00
[Svelte-url]: https://svelte.dev/
[Laravel.com]: https://img.shields.io/badge/Laravel-FF2D20?style=for-the-badge&logo=laravel&logoColor=white
[Laravel-url]: https://laravel.com
[Bootstrap.com]: https://img.shields.io/badge/Bootstrap-563D7C?style=for-the-badge&logo=bootstrap&logoColor=white
[Bootstrap-url]: https://getbootstrap.com
[JQuery.com]: https://img.shields.io/badge/jQuery-0769AD?style=for-the-badge&logo=jquery&logoColor=white
[JQuery-url]: https://jquery.com 
