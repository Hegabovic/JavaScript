<div id="top"></div>

[//]: # ([![LinkedIn][linkedin-shield]][linkedin-url])

<!-- PROJECT LOGO -->
<br />
<div align="center">
  <a href="https://github.com/Hegabovic/JavaScript.git">
    <img src="images/logo.png" alt="Logo" width="80" height="80">
  </a>

<h3 align="center">Understand JavaScript</h3>

  <p align="center">
    from zero to hero tutorial
    <br />
    <a href="https://github.com/Hegabovic/JavaScript.git"><strong>Explore the docs »</strong></a>
    <br />
    <br />
    <a href="https://github.com/Hegabovic/JavaScript.git">View Demo</a>
    ·
    <a href="https://github.com/Hegabovic/issues">Report Bug</a>
    ·
    <a href="https://github.com/Hegabovic/issues">Request Feature</a>
  </p>
</div>



<!-- TABLE OF CONTENTS -->
<details>
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#about-the-course">About The Course</a>
      <ul>
        <li><a href="#built-with">Built With</a></li>
      </ul>
    </li>
    <li>
      <a href="#JavaScript Features">JavaScript Features</a>
      <ul>
        <li><a href="#Type system of JS ">Type system of JS </a></li>
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
## about-the-course
javascript has many features, a long the way you will understand every point of the following
after studying the following you will have a solid background to kick-start your career in JS

<p align="right">(<a href="#top">back to top</a>)</p>

<!-- JavaScript Features -->
## JavaScript Features
1. Loosely type language: not strongly typed language <br>
Variables type will be determined according to its value, note that you can know 
the type of any variable using `typeof(variable-name);` or `typeof variable-name; ` and it returns small letter
```sh 
var x;           // type of x is undefined (not initlized)
var x = 10;      // type of x is number
var x = "ITI";   // type of x is string
```
2. Object based language
   * User defined objects
   * Language objects (Numbers, Math, Date, String,...)
   * Browser objects also called BOM (navigator, window, History)
   * HTML objects also called DOM 
3. Interpreted language <br>
it isn't a compiled language, and it operates from top to bottom : left to right
4. event handling 
5. Integrated with HTML 
6. Case Sensitive <br>
`var a;` is very different from `var A;`

## Type system of JS 
1. primitive types 
   * Undefined
   * String
   * Number
   * Null
   * boolean
2.Object types
   * Date
   * Array
   
## Where To Write JS
### internal script 
1. internal HTML: Within script tag 
```sh
    <head>
        <script>
              // code
        </script>
    </head>
```
2. allowed writing Script codes inside body tag within script
```sh
    <body>
        <script>
              // code
        </script>
    </body>
```
3. inline script: event handling scripts
```sh
 <button onclick="function call();"/>   
```
### external script
 - put script tag `<script></script>` before the end of the body tag.
```sh
    <body>
        
        <script src="test.js" ></script>
    </body>
```
 - javascript is a client side language so the user might close script running from browser settings.
```sh
 <noscript>
  <h3> Enable JS </h3>
 </noscript>   
```

<p align="right">(<a href="#top">back to top</a>)</p>

## Primitive type variables
- semicolon `;` is optional in JS. <br>
- `null` is used to reset reference.<br>
```sh
 var x ;         // Without initial value : variable from type undefined : undefined
 var x = 10;     // x value =  10  from type: number
 var x = "ITI";  // x value =  ITI from type: string
 var x = true;   // x value = true from type: boolean
 var x = null;   // x value = null from type: `OBJECT`  
```
### Number type
to declare variable from type number:
1. literal creation 
 ```sh
   var x = 10;  // from type `Number`: prototype name : object Name 
 ```
2. constructor creation: use keyword `new` plus `prototype` name.
 
<!-- USAGE EXAMPLES -->
## Usage

Use this space to show useful examples of how a project can be used. Additional screenshots, code examples and demos work well in this space. You may also link to more resources.

_For more examples, please refer to the [Documentation](https://example.com)_

<p align="right">(<a href="#top">back to top</a>)</p>



<!-- ROADMAP -->
## Roadmap

- [ ] Feature 1
- [ ] Feature 2
- [ ] Feature 3
    - [ ] Nested Feature

See the [open issues](https://github.com/github_username/repo_name/issues) for a full list of proposed features (and known issues).

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

Your Name - [@twitter_handle](https://twitter.com/twitter_handle) - email@email_client.com

Project Link: [https://github.com/github_username/repo_name](https://github.com/github_username/repo_name)

<p align="right">(<a href="#top">back to top</a>)</p>



<!-- ACKNOWLEDGMENTS -->
## Acknowledgments

* []()
* []()
* []()

<p align="right">(<a href="#top">back to top</a>)</p>



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
