<!-- PROJECT LOGO -->
<br />
<p align="center">
  <a href="https://github.com/Chetan-Goyal/How-to-deploy-First-DAPP-Template">
    <img src="readme_images/DAPP.png" alt="Logo" width="80" height="80">
  </a>

  <h3 align="center">Deploying First DAPP Template</h3>

  <p align="center">
    Making Environment Setup for developing DAPPS Easier !
    <br />
    

<!-- TABLE OF CONTENTS -->
<details open="open">
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#about-the-project">About The Project</a>
    </li>
    <li>
      <a href="#getting-started">Getting Started</a>
      <ul>
        <li><a href="#prerequisites">Prerequisites</a></li>
        <li><a href="#installation">Installation</a></li>
      </ul>
    </li>
    <li><a href="#usage">Usage</a></li>
    <li><a href="#contributing">Contributing</a></li>
    <li><a href="#license">License</a></li>
    <li><a href="#contact">Contact</a></li>
    <li><a href="#acknowledgements">Acknowledgements</a></li>
  </ol>
</details>



<!-- ABOUT THE PROJECT -->
## About The Project

[![Product Name Screen Shot][product-screenshot]](https://example.com)

If you want to build your first DAPP or want to use a simple DAPP as template, this is the right place for you.  Deploying first DAPP is always difficult. That's why, I will try to guide you through the easiest way for deploying your first DAPP.

Of course, no one template will serve all projects since your needs may be different. But after deploying your first DAPP, you will be able to understand how DAPP works. I'll be adding more templates in the near future. You may also suggest changes by forking this repo and creating a pull request or opening an issue. Thanks to all the people have have contributed to expanding this template!

A list of commonly used resources that I find helpful are listed in the acknowledgements.

### Built With

* [Node](https://nodejs.org/en/)
* [Ganache CLI](https://github.com/trufflesuite/ganache-cli)
* [Solidity compiler](https://github.com/ethereum/solc-js)

<!-- GETTING STARTED -->
## Getting Started

Make sure you follow each and every step carefully as written here otherwise you may get stuck at nowhere (telling from experience :P)

## Prerequisites

* **Node.js  (Version Used: `v10.14.2`)**
	  
	```sh
	# Linux Users
	sudo apt install nodejs

	# Mac Users
	brew install node
	```
*Windows Users*, visit [Node.js Website](https://nodejs.org/en/download/)

* **npm (Version Used: `6.4.1`)**

  ```sh
  npm install npm@latest -g
  ```

* **Solc-js (Version Used: `0.8.0`)**
	```sh
	npm i solc-js
	```
	
### Installation

1. Register on [https://infura.io/](https://infura.io/) and create a new project.
2. After creating project, you will see that there will be 2 Endpoints. It will be used later in our project.
3. Clone the repo
   ```sh
   git clone https://github.com/Chetan-Goyal/How-to-deploy-First-DAPP-Template.git
   cd How-to-deploy-First-DAPP-Template/
   ```
4. Install NPM packages
   ```sh
   npm install
   ```

6. Now run the following command to globally install the  `npx`  module.
	```sh
	npm install -g npx
	```



<!-- USAGE EXAMPLES -->
## Usage

1. Run the below command command-
   ```sh
   solcjs --bin --abi -o ./build FirstContract.sol
   ```
   *(Above command will create a directory named `build` with two files.)*
2. Now, create a new terminal and navigate to the project directory using `cd`. Here, we are going to run our instance of Ganache. *Replace the `<ENDOPOINT>` with the https endpoint you have received from Infura.io at 2nd Step of Installation.* 
	```sh
	cd first-ethereum-dapp/
	npx ganache-cli -f <ENDPOINT>
	```
3. Run the following command
	```sh
	node deploy.js
	```
	*(If you are getting errors here, make sure that the filenames mentioned in deploy.js are same as the filenames inside build `directory`)*

4. If successful, you will see the following output on your command line.

	```sh
	FirstContract was successfully deployed!  
	FirstContract can be interfaced with at this address:  
	0x702f935d608Aadf90323310c489B2903af20AA43
	```
	You will get a different address here.
5. Copy the address which you received here in `myContractAddress` variable with quotes in `index.html`.
6. Now, Open `build/FirstContract_sol_FirstContract.abi` and copy all of it's content. Paste the copied content in `myAbi` variable in place of `[]` in `index.html.`
7. Now, we are ready to run our DAPP. Run the following command:
	```sh
	npx http-server
	```
	If you received receive the following response in your terminal,
	```sh
	Starting up http-server, serving ./
	Available on:
	  http://127.0.0.1:8080
	Hit CTRL-C to stop the server	
	```
Hurray!! You have finally run your first DAPP. Now, go to the above url. You will see your DAPP up and running.



_If you liked this guide, give it a ⭐ and don't forget to follow for more amazing upcoming projects. :D_



<!-- ROADMAP -->
## Roadmap

See the [open issues](https://github.com/Chetan-Goyal/How-to-deploy-First-DAPP-Template/issues) for a list of proposed features (and known issues).



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

Chetan Goyal - chetangoyal@ddu.du.ac.in

Project Link: [https://github.com/Chetan-Goyal/How-to-deploy-First-DAPP-Template](https://github.com/Chetan-Goyal/How-to-deploy-First-DAPP-Template)



<!-- ACKNOWLEDGEMENTS -->
## Acknowledgements
* [Setting up an Ethereum Development Environment](https://medium.com/compound-finance/setting-up-an-ethereum-development-environment-7c387664c5fe)
* [NPM](https://www.npmjs.com/)

