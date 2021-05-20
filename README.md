
[![Contributors][contributors-shield]][contributors-url]
[![Forks][forks-shield]][forks-url]
[![Stargazers][stars-shield]][stars-url]
[![Issues][issues-shield]][issues-url]
[![MIT License][license-shield]][license-url]
[![LinkedIn][linkedin-shield]][linkedin-url]

<!-- PROJECT LOGO -->
<br />
<p align="center">
  <a href="https://github.com/othneildrew/Best-README-Template">
    <img src="images/logo.png" alt="Logo" width="80" height="80">
  </a>

  <h3 align="center">Python SQL Intro</h3>

  <p align="center">
    Introduccion de como usar Python Y SQL (SSMS)
    <br />
    <a href="https://github.com/othneildrew/Best-README-Template">View Demo</a>
    ·
    <a href="https://github.com/othneildrew/Best-README-Template/issues">Report Bug</a>
    ·
    <a href="https://github.com/othneildrew/Best-README-Template/issues">Request Feature</a>
  </p>
</p>

<!-- TABLE OF CONTENTS -->
<details open="open">
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#about-the-project">Todo lo que tienes que Saber</a>
      <ul>
        <li><a href="#built-with">Construido Con</a></li>
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
    <li><a href="#acknowledgements">Acknowledgements</a></li>
  </ol>
</details>



<!-- ABOUT THE PROJECT -->
## About The Project

[![Product Name Screen Shot][product-screenshot]](https://example.com)

There are many great README templates available on GitHub, however, I didn't find one that really suit my needs so I created this enhanced one. I want to create a README template so amazing that it'll be the last one you ever need -- I think this is it.

Here's why:
* Your time should be focused on creating something amazing. A project that solves a problem and helps others
* You shouldn't be doing the same tasks over and over like creating a README from scratch
* You should element DRY principles to the rest of your life :smile:

Of course, no one template will serve all projects since your needs may be different. So I'll be adding more in the near future. You may also suggest changes by forking this repo and creating a pull request or opening an issue. Thanks to all the people have have contributed to expanding this template!

```bash

import socket
import time    
import pyodbc

maquina = socket.gethostname()

cnxn = pyodbc.connect(
    "Driver={SQL Server Native Client 11.0};"
    "Server=MKTCRM;"
    "Database=RPyA;"
    "Trusted_Connection=yes"
)

print(f"La maquina ejecutando este script es: {maquina}")

def insert(cnxn,maquina):
    fecha = time.strftime('%Y-%m-%d %H:%M:%S')
    print(f"Insertar bbdd a las {fecha}")
    cursor = cnxn.cursor()
    cursor.execute('Insert into [RPyA].[dbo].[ProcesosPruebas](Fecha,Proceso,Servidor,Extras) values(?, ?, ?, ?)', (fecha,'Pruebas DT', maquina ,'Adicionales Prueba')
    )
"""     cursor.commit()
    cursor.close()
    cnxn.close() """

for i in range(10):
    insert(cnxn,maquina)

```

### Construido con

This section should list any major frameworks that you built your project using. Leave any add-ons/plugins for the acknowledgements section. Here are a few examples.
* [Bootstrap](https://getbootstrap.com)
* [JQuery](https://jquery.com)
* [Laravel](https://laravel.com)
* https://github.com/othneildrew/Best-README-Template/blob/master/README.md



<!-- GETTING STARTED -->
## Getting Started

Instalar Python -> PIP -> install pyodbc

### Prerequisites

This is an example of how to list things you need to use the software and how to install them.
* Python
* PIP
  ```sh
  pip install pyodbc
  ```

### Installation

1. Instalar Python en [https://www.python.org/downloads/](https://example.com)
2. Clone the repo
   ```sh
   git clone https://github.com/jpgmia/PythonSQLIntro/edit/main/README.md
   ```
3. Install PIP packages
   ```sh
   pip install pyodbc
   ```
4. Enter codigo API in `config.js`
```bash

import socket
import time    
import pyodbc

maquina = socket.gethostname()

cnxn = pyodbc.connect(
    "Driver={SQL Server Native Client 11.0};"
    "Server=MKTCRM;"
    "Database=RPyA;"
    "Trusted_Connection=yes"
)

print(f"La maquina ejecutando este script es: {maquina}")

def insert(cnxn,maquina):
    fecha = time.strftime('%Y-%m-%d %H:%M:%S')
    print(f"Insertar bbdd a las {fecha}")
    cursor = cnxn.cursor()
    cursor.execute('Insert into [RPyA].[dbo].[ProcesosPruebas](Fecha,Proceso,Servidor,Extras) values(?, ?, ?, ?)', (fecha,'Pruebas DT', maquina ,'Adicionales Prueba')
    )
"""     cursor.commit()
    cursor.close()
    cnxn.close() """

for i in range(10):
    insert(cnxn,maquina)

```



<!-- USAGE EXAMPLES -->
## Usage

Use this space to show useful examples of how a project can be used. Additional screenshots, code examples and demos work well in this space. You may also link to more resources.

_For more examples, please refer to the [Documentation](https://example.com)_



<!-- ROADMAP -->
## Roadmap

See the [open issues](https://github.com/othneildrew/Best-README-Template/issues) for a list of proposed features (and known issues).



<!-- CONTRIBUTING -->
## Contribuir

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

Testing Autoamtion- [@your_twitter](https://twitter.com/your_username) - email@example.com

Project Link: [https://github.com/jpgmia/PythonSQLIntro](https://github.com/jpgmia/PythonSQLIntro)



<!-- ACKNOWLEDGEMENTS -->
## Acknowledgements
* [Template Designer](https://github.com/othneildrew/Best-README-Template/blob/master/README.md)
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
[contributors-shield]: https://img.shields.io/github/contributors/othneildrew/Best-README-Template.svg?style=for-the-badge
[contributors-url]: https://github.com/othneildrew/Best-README-Template/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/othneildrew/Best-README-Template.svg?style=for-the-badge
[forks-url]: https://github.com/othneildrew/Best-README-Template/network/members
[stars-shield]: https://img.shields.io/github/stars/othneildrew/Best-README-Template.svg?style=for-the-badge
[stars-url]: https://github.com/othneildrew/Best-README-Template/stargazers
[issues-shield]: https://img.shields.io/github/issues/othneildrew/Best-README-Template.svg?style=for-the-badge
[issues-url]: https://github.com/othneildrew/Best-README-Template/issues
[license-shield]: https://img.shields.io/github/license/othneildrew/Best-README-Template.svg?style=for-the-badge
[license-url]: https://github.com/othneildrew/Best-README-Template/blob/master/LICENSE.txt
[linkedin-shield]: https://img.shields.io/badge/-LinkedIn-black.svg?style=for-the-badge&logo=linkedin&colorB=555
[linkedin-url]: https://linkedin.com/in/othneildrew
[product-screenshot]: images/screenshot.png
