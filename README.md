<p align="center">
<br/><br/>
<img src="https://avatars1.githubusercontent.com/u/24256542?v=3&s=200" alt="UNI logo"/>
</p>

<br/><br/>

<h1 align="center">UNI</h1>
<p align="center">
A universal and optimized interface for handle package managers on Linux distributions.<br/><br/>
<a href="#"><img src="https://img.shields.io/badge/uni-v0.2.0-blue.svg" alt="version"/></a>
<a href="#"><img src="https://img.shields.io/badge/support-ubuntu%3A%20apt%20%7C%20fedora%3A%20dnf%20-lightgrey.svg" alt="support"/></a>
<a href="https://github.com/daltonmenezes/uni/blob/master/LICENSE"><img src="https://img.shields.io/github/license/mashape/apistatus.svg" alt="license"/></a>
</p>

<br/>

> UNI is an abstraction layer that allows you to manage different package managers using the same UNI commands regardless of the distribution you are using and automates repetitive tasks on them.

<br/>

# Table of Contents

- [Goal](#goal)
- [How it Works?](#how-it-works)
  - [Example](#example)
- [Using Recipes](#using-recipes)
  - [Example](#example-1)
- [Installation](#installation)
- [Uninstallation](#uninstallation)
- [Documentation](#documentation)
- [Contributing](#contributing)

# Goal

The goal is make an easy interface that abstracts repetitive commands related to package management. Join tasks that require the execution of others without spending time typing one by one. Make it easy to work between different distributions by always using the same UNI commands regardless of the distribution you are using.

# How it Works?

UNI uses your main package manager to do the things and abstracts the original commands through a simple and universal UNI interface.

## Example

| Command | Alias | Description |
| --- | --- | --- |
| `uni upgrade` | `uni up`  | Upgrades deeply the system and remove useless dependencies. |

This will trigger the following commands on **Ubuntu**:
```shell
sudo apt-get update
sudo apt-get upgrade -y
sudo apt-get dist-upgrade -y
sudo apt-get autoremove -y
```
This will trigger the following commands on **Fedora**:
```shell
sudo dnf upgrade -y
sudo dnf autoremove -y
```
# Using Recipes

Now you can use available recipes too or create your owns and publish it [here](https://github.com/uni-linux/recipes). Recipes are bash scripts to do anything. Be it to install programs and resolve dependencies or fix system problems. Anything you want and can do with bash scripts.

## Example

| Command | Alias | Description |
| --- | --- | --- |
| `uni bake daltonmenezes/atom-install` | `uni b daltonmenezes/atom-install`  | Installs the latest version of<br/>Atom Editor from their<br/>official website and resolve<br/>dependency issues. |

[Check here the list of available recipes for usage.](https://github.com/uni-linux/recipes)

# Installation

**Ubuntu** and based distributions:
```shell
wget -O upm https://git.io/v1UKq && chmod +x upm && ./upm && rm upm
```
**Fedora** ( supports only dnf for now ):
```shell
wget -O upm https://git.io/v1UKO && chmod +x upm && ./upm && rm upm
```
# Uninstallation

| Command | Alias |
| --- | --- | --- |
| `uni remove-me` | `uni rm-me` |

# Documentation

- [English](https://github.com/daltonmenezes/uni/blob/master/docs/en/API.md)
- Português (Em breve)

# Contributing

I've created a 'recompiler' tool to help us to test locally using uni command on terminal normally during the development.

[So, let's check the contributing guide here](https://github.com/daltonmenezes/uni/blob/master/docs/en/CONTRIBUTING.md).
