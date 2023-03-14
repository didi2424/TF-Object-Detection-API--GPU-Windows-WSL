 <a name="readme-top"></a>

<!-- The Basics -->
## The Basics

This repository is a tutorial for how to use Tensorflow's Object Detection API (boxes Classsifier) to train an image into object detection classifier on Windows 11 Host. also when Tensorflow 2.11 is not support GPU inside Windows anymore, so we can use Ubuntu on Windows as our main host.


This README.md describes every step required to get going with your custom object detection classifier :

<!-- TABLE OF CONTENTS -->
<details>
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#the-basics">The Basics</a>
    </li>
    <li>
    <a href="#about-the-project">About The Project</a>
    <ul>
        <a href="#build-with"> Build With </a>
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
    <li><a href="#roadmap">Roadmap</a></li>
    <li><a href="#contributing">Contributing</a></li>
    <li><a href="#license">License</a></li>
    <li><a href="#contact">Contact</a></li>
    <li><a href="#acknowledgments">Acknowledgments</a></li>
  </ol>
</details>

<!-- ABOUT THE PROJECT -->
## About The Project

The purpose of this tutorial is to explain how to train you custom Convolutional Neural Network Object Detection Classifier with your custom image and Models that Tensorflow Provide, Also in this tutorial you will use a powerfull 'Jupyter Notebook' for interface and connect to your 'Ubuntu On Windows' At the end of this tutorial, you will have a program that can identify object with draw boxes around specific objects in pictures, videos, or in the webcam feed.

Serveral Good Tutorial avaliable in github for how to use Tensorflow Object Detection API. Hovewer in this tutorial that use Tensorflow version 2.11. Tensorflow >= 2.11 will no longger supported on Windows for GPU usage. Tensorflow for future version seems using Linux for supported GPU usage.  
If you don't like to dual boot this is good tutorial for you ❤️


<p align="right">(<a href="#readme-top">back to top</a>)</p>

### Environment on Windows 10/11
* [![Windows][Windows]][Windows-url]
* [![Nvidia][Nvidia]][Nvidia-url]


### Built With

* [![Tensorflow][Tensorflow]][Next-url]
* [![Python][Python]][Python-url]
* [![Ubuntu][Ubuntu]][Ubuntu-url]
* [![Nvidia][Nvidia]][Nvidia-url]
* [![Jupyter-Notebook][Jupyter-Notebook]][Jupyter-Notebook-url]
* [![Miniconda][Miniconda]][Miniconda-url]


<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- GETTING STARTED -->
## Getting Started

Tensorflow's GPU allows your PC to use the graphic card to provide extra processing power while training the dataset and the models, so it will be used for this tutoral, in the air GPU provide faster training dataset than CPU. Nowday Tensorflow => 2.11 is not supporting Windows to use a GPU. So, you are need 'Ubuntu on Windows' to solve this.



### Environment in Windows

_Enable you windows WSL_
1. Click Start on your windows and search Windows Features
2. in the Windows Features Find And Enable
   ```sh
   Enable Virtual Machine Platfrom
   Enable Windows WSL
   ```
3. Click Ok 



_Downloads Ubuntu on Windows_
1. Click Start on your windows and search Microsoft Store
2. on search bar Type
   ```sh
   Ubuntu on Windows
   ```
3. Click Get

4. After downloading and instaling Ubuntu on Windows Apps will appear in _Start Menu_
5. First time you open Ubuntu on Windows you need to configure the ubuntu name and password.

<p align="right">(<a href="#readme-top">back to top</a>)</p>

### Environment in Ubuntu on Windows _(WSL)_
_Install Miniconda 3 inside WSL_
1. Open your WSL and Command
   ```sh
   sudo apt-get update
   sudo apt-get install wget
   ```
2. Download Miniconda for Linux and install
   ```sh
   wget https://repo.anaconda.com/miniconda/Miniconda3-py38_23.1.0-1-Linux-x86_64.sh
   sh ./Miniconda3-py39_4.12.0-Linux-x86_64.sh
   ```
3. Wait until installation is finished
4. After Miniconda installation is done you need make an env (in this tutorial we named env to 'tfod') with python 3.8.10
   ```sh
   conda create --name tfod python=3.8.10 -y
   conda deactivate
   ```
5. Install Cuda Driver for Windows WSL
   ```sh
   wget https://developer.download.nvidia.com/compute/cuda/repos/wsl-ubuntu/x86_64/cuda-wsl-ubuntu.pin
   sudo mv cuda-wsl-ubuntu.pin /etc/apt/preferences.d/cuda-repository-pin-600
   wget https://developer.download.nvidia.com/compute/cuda/12.1.0/local_installers/cuda-repo-wsl-ubuntu-12-1-local_12.1.0-1_amd64.deb
   sudo dpkg -i cuda-repo-wsl-ubuntu-12-1-local_12.1.0-1_amd64.deb
   sudo cp /var/cuda-repo-wsl-ubuntu-12-1-local/cuda-*-keyring.gpg /usr/share/keyrings/
   sudo apt-get update
   sudo apt-get -y install cuda
   ```
6. Activate the env 
   ```sh
   conda activate tfod
   ```
7. Install Jupyter Notebook for our Interface to the env
   ```sh
   conda install jupyter notebook -y
   ``` 
8. Run Jupyter notebook
   ```sh
   Jupyter Notebook
   ```
<p align="right">(<a href="#readme-top">back to top</a>)</p>





<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
[contributors-shield]: https://img.shields.io/github/contributors/github_username/repo_name.svg?style=for-the-badge
[contributors-url]: https://github.com/github_username/repo_name/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/github_username/repo_name.svg?style=for-the-badge
[forks-url]: https://github.com/github_username/repo_name/network/members
[stars-shield]: https://img.shields.io/github/stars/github_username/repo_name.svg?style=for-the-badge
[stars-url]: https://github.com/github_username/repo_name/stargazers
[issues-shield]: https://img.shields.io/github/issues/github_username/repo_name.svg?style=for-the-badge
[issues-url]: https://github.com/github_username/repo_name/issues
[license-shield]: https://img.shields.io/github/license/github_username/repo_name.svg?style=for-the-badge
[license-url]: https://github.com/github_username/repo_name/blob/master/LICENSE.txt
[linkedin-shield]: https://img.shields.io/badge/-LinkedIn-black.svg?style=for-the-badge&logo=linkedin&colorB=555
[linkedin-url]: https://linkedin.com/in/linkedin_username
[product-screenshot]: images/screenshot.png
[Next.js]: https://img.shields.io/badge/next.js-000000?style=for-the-badge&logo=nextdotjs&logoColor=white
[Next-url]: https://nextjs.org/
[Tensorflow]: https://img.shields.io/badge/Tensorflow-000000?style=for-the-badge&logo=Tensorflow&logoColor=orange
[Tensorflow-url]: https://www.tensorflow.org/
[Python]: https://img.shields.io/badge/Python-000000?style=for-the-badge&logo=Python&logoColor=blue
[Python-url]: https://www.python.org/
[Ubuntu]: https://img.shields.io/badge/Ubuntu-000000?style=for-the-badge&logo=Ubuntu&logoColor=orange
[Ubuntu-url]: https://ubuntu.com/wsl
[Nvidia]: https://img.shields.io/badge/Nvidia-000000?style=for-the-badge&logo=Nvidia&logoColor=green
[Nvidia-url]: https://ubuntu.com/wsl
[Jupyter-Notebook]: https://img.shields.io/badge/Jupyter/Notebook-000000?style=for-the-badge&logo=Jupyter&logoColor=orange
[Jupyter-Notebook-url]: https://jupyter.org/
[Windows]: https://img.shields.io/badge/Windows/WSL-000000?style=for-the-badge&logo=windows&logoColor=blue
[Windows-url]: https://jupyter.org/
[miniconda]: https://img.shields.io/badge/Miniconda-000000?style=for-the-badge&logo=Anaconda&logoColor=green
[miniconda-url]: https://jupyter.org/

