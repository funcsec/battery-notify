<div id="top"></div>

[![Contributors][contributors-shield]][contributors-url]
[![Forks][forks-shield]][forks-url]
[![Stargazers][stars-shield]][stars-url]
[![Issues][issues-shield]][issues-url]
[![MIT License][license-shield]][license-url]


<h3 align="center">Battery Notify</h3>

  <p align="center">
    Know when you need to run to the charger
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
    <li><a href="#contributing">Contributing</a></li>
    <li><a href="#license">License</a></li>
    <li><a href="#contact">Contact</a></li>
  </ol>
</details>



<!-- ABOUT THE PROJECT -->
## About The Project

Very simple script and systemd timer/service for notifying you when your laptop charge is low and you need to run to the charger. 

Great for using [i3wm](https://i3wm.org/) or other minimal windows managers that lack desktop environment perks.

Timer runs every 5 minutes and notifies when the battery life drops below 15%. Does not Suspend or Hibernate computer, runs with user priviledges. 

<p align="right">(<a href="#top">back to top</a>)</p>

### Built With

* systemd
* bash
* linux
* stow

<p align="right">(<a href="#top">back to top</a>)</p>



<!-- GETTING STARTED -->
## Getting Started

This is an example of how you may give instructions on setting up your project locally.
To get a local copy up and running follow these simple example steps.

### Prerequisites

The project requires Linux with systemd, notify-send, and stow. 


```sh
sudo apt update 
sudo apt install stow -y
```

### Installation


1. Clone the repo
   ```sh
   git clone https://github.com/funsec/battery-notify.git $HOME/.dotfiles/battery-notify
   ```
2. Use `stow` to link the files into the correct directories
   ```sh
   cd $HOME/.dotfiles/battery-notify
   stow -vt $HOME/ battery-notify
   ```
3. Reload user systemd daemon 
   ```sh
   systemctl --user daemon-reload
   ```
4. Start and enable user systemd timer
   ```sh
   systemctl --user enable battery-notify.timer
   systemctl --user start battery-notify.timer
   ```
5. Let you battery run below 15% to test the notifications

<p align="right">(<a href="#top">back to top</a>)</p>


<!-- CONTRIBUTING -->
## Contributing

Contributions are what make the open source community such an amazing place to learn, inspire, and create. Any contributions you make are **greatly appreciated**.

If you have a suggestion that would make this better, please fork the repo and create a pull request. You can also simply open an issue with the tag "enhancement".
Don't forget to give the project a star! Thanks again!

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

<p align="right">(<a href="#top">back to top</a>)</p>



<!-- LICENSE -->
## License

Distributed under the MIT License. See `LICENSE.txt` for more information.

<p align="right">(<a href="#top">back to top</a>)</p>



<!-- CONTACT -->
## Contact

funcsec - [@funcsec](https://twitter.com/funcsec)

Project Link: [https://github.com/funsec/battery-notify](https://github.com/funsec/battery-notify)

<p align="right">(<a href="#top">back to top</a>)</p>



<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
[contributors-shield]: https://img.shields.io/github/contributors/github_username/repo_name.svg?style=for-the-badge
[contributors-url]: https://github.com/funsec/battery-notify/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/github_username/repo_name.svg?style=for-the-badge
[forks-url]: https://github.com/funsec/battery-notify/network/members
[stars-shield]: https://img.shields.io/github/stars/github_username/repo_name.svg?style=for-the-badge
[stars-url]: https://github.com/funsec/battery-notify/stargazers
[issues-shield]: https://img.shields.io/github/issues/github_username/repo_name.svg?style=for-the-badge
[issues-url]: https://github.com/funsec/battery-notify/issues
[license-shield]: https://img.shields.io/github/license/github_username/repo_name.svg?style=for-the-badge
[license-url]: https://github.com/funsec/battery-notify/blob/master/LICENSE.txt
[product-screenshot]: images/screenshot.png

