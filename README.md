<!--
*** Thanks for checking out this README Template. If you have a suggestion that would
*** make this better, please fork the repo and create a pull request or simply open
*** an issue with the tag "enhancement".
*** Thanks again! Now go create something AMAZING! :D
-->

<h1>Red Ball Follower Robot<h1>


<!-- TABLE OF CONTENTS -->
## Table of Contents

* [About the Project](#about-the-project)
  * [Built With](#built-with)
* [Getting Started](#getting-started)
  * [Prerequisites](#prerequisites)
  * [Installation](#installation)
* [Usage](#usage)
* [Roadmap](#roadmap)
* [Contributing](#contributing)
* [License](#license)
* [Contact](#contact)
* [Acknowledgements](#acknowledgements)



<!-- ABOUT THE PROJECT -->
## About The Project


I made this project in order to build a basic ball tracking car. Here, my bot uses camera to take frames and do image processing to track down the ball. The features of the ball such as color, shape, size can be used.I have chosen raspberry pi as micro-controller for this project as it gives great flexibility to use Raspberry Pi camera module and allows to code in Python which is very user friendly and OpenCV library, for image analysis.

For controlling the motors, I have used an H-Bridge to switch from clockwise to counter-clockwise or to stop the motors. This I have integrated via code when direction and speed has to be controlled in different obstacle situations.

Crucial thing while detecting images frame by frame was to avoid any frame drops as then the bot can go into a limbo state if the bot is unable to predict direction of ball after few frame drops. Even if it manage the frame drops then also if the ball goes out of scope of the camera, it will go into a limbo state, in that case, then I have made my bot take a 360 degree view of it's environment till the ball comes back in the scope of the camera and then start moving in it's direction.

For the image analysis, I am taking each frame and then masking it with the color needed. Then for noise reduction, I am eroding the noise and dilating the major blobs. Then I find all the contours and find the largest among them and bound it in a rectangle. And show the rectangle on the main image and find the coordinates of the center of the rectangle.I have attached the algorithm (pseudo-code) of the image analysis part and demonstrated this part in the video also. 

Finally my bot tries to bring the coordinates of the ball to the center of its imaginary coordinate axis. This is how my robo works. I enjoy a lot working on this project and its a nice experience.

### Built With
1. Raspberry pi (any version) with raspbian os installed
2. 3 Ultrasonic sensors 
3. Motor driver (LM298 , L293D module)
4. Power supply
5. Jumper cambles (Feamle-female)
6. Camera module(use module over usb camera for better camera)
7. Red ball for testing 

### Prerequisites


1. Python2
2. opencv -3.10
3. picamera
4. Raspberry-pi with raspbian os installed


### Installation

1. Create a python file in raspberry pi
```sh
 sudo nano filename.py```
2. Install NPM packages
```sh
npm install
```
4. Enter your API in `config.js`
```JS
const API_KEY = 'ENTER YOUR API';
```



<!-- USAGE EXAMPLES -->
## Usage

Use this space to show useful examples of how a project can be used. Additional screenshots, code examples and demos work well in this space. You may also link to more resources.

_For more examples, please refer to the [Documentation](https://example.com)_



<!-- ROADMAP -->
## Roadmap

See the [open issues](https://github.com/othneildrew/Best-README-Template/issues) for a list of proposed features (and known issues).



<!-- CONTRIBUTING -->
## Contributing

Contributions are what make the open source community such an amazing place to be learn, inspire, and create. Any contributions you make are **greatly appreciated**.

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request



<!-- LICENSE -->
## License

Distributed under the MIT License. See `LICENSE` for more information.



<!-- CONTACT -->
## Contact

Your Name - [@your_twitter](https://twitter.com/your_username) - email@example.com

Project Link: [https://github.com/your_username/repo_name](https://github.com/your_username/repo_name)



<!-- ACKNOWLEDGEMENTS -->
## Acknowledgements
* [GitHub Emoji Cheat Sheet](https://www.webpagefx.com/tools/emoji-cheat-sheet)
* [Img Shields](https://shields.io)
* [Choose an Open Source License](https://choosealicense.com)
* [GitHub Pages](https://pages.github.com)
* [Animate.css](https://daneden.github.io/animate.css)
* [Loaders.css](https://connoratherton.com/loaders)
* [Slick Carousel](https://kenwheeler.github.io/slick)
* [Smooth Scroll](https://github.com/cferdinandi/smooth-scroll)
* [Sticky Kit](http://leafo.net/sticky-kit)
* [JVectorMap](http://jvectormap.com)
* [Font Awesome](https://fontawesome.com)





<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
[contributors-shield]: https://img.shields.io/github/contributors/othneildrew/Best-README-Template.svg?style=flat-square
[contributors-url]: https://github.com/othneildrew/Best-README-Template/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/othneildrew/Best-README-Template.svg?style=flat-square
[forks-url]: https://github.com/othneildrew/Best-README-Template/network/members
[stars-shield]: https://img.shields.io/github/stars/othneildrew/Best-README-Template.svg?style=flat-square
[stars-url]: https://github.com/othneildrew/Best-README-Template/stargazers
[issues-shield]: https://img.shields.io/github/issues/othneildrew/Best-README-Template.svg?style=flat-square
[issues-url]: https://github.com/othneildrew/Best-README-Template/issues
[license-shield]: https://img.shields.io/github/license/othneildrew/Best-README-Template.svg?style=flat-square
[license-url]: https://github.com/othneildrew/Best-README-Template/blob/master/LICENSE.txt
[linkedin-shield]: https://img.shields.io/badge/-LinkedIn-black.svg?style=flat-square&logo=linkedin&colorB=555
[linkedin-url]: https://linkedin.com/in/othneildrew
[product-screenshot]: images/screenshot.png
