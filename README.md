# CMake_templates
This project is a storage for different project type templates using [CMake](https://cmake.org/overview/).

## Structure
Repo contains dfferent project teemplates. They are classified using folder structure. Every project should be referenced from common content page _(todo: when teplates will be commented, extract content or comments from this file)_.

Teplate contains not only cmake files but also `mock_` files. They could be used for test or as an example or usage. `mock_` floders and even projects are allowed.

## For committers

Originally made for students of [Applyed math dpt. of SPbSTU](https://iamm.spbstu.ru/department/kafedra_prikladnaya_matematika/), this project may be used and enriched by anyone.
Introducing your own template, please, follow principles listed below:
* Style: try to follow already used code style
* Actomicness: Make your templates atomic, exclude all parts not related to its main purpose
* Interface reduction: Keep a limited number of modification points in you files. Extract them if it is possible. Keep theem well commented and well visible

## Content
* Basic templates
  * [Single target](basic_templates/single_target)
