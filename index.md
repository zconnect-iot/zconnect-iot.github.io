---
layout: default
---

ZConnect is an open-source connected product development toolkit. Add
connectivity and smart features to an existing line of devices, or  create an
entirely new product with the endless possibilities that connected devices
unlock.

<div class="row-of-boxes">
<div class="box"><div markdown="1">

### Django App

The ZConnect Django app makes it really easy to build a powerful, scalable
backend for your connected product. Built-in functionality for:

- interfacing with devices
- storing and aggregating time-series data
- managing users, organizations and billing

</div>
<a class="btn">Learn more</a>
</div>
<div class="box"><div markdown="1">

### Frontend Framework

The ZConnect front-end libraries, built with React and Redux to enable extremely fast
development of web interfaces and apps

- **zconnect-js** provides core functionality for use across React and React Native applications
- **zconnect-web** is a flexible and powerful collection of React components for quickly building UIs.

</div>
<a class="btn">Learn more</a>
</div>
</div>

# System overview

A typical IoT deployment is devided into three main parts: the IoT platform, the devices and the interfaces to interact with the system. In Zconnect, the IoT platform can be built on top of `zconnect-django`, the devices communicate with the platform over MQTT and the interfaces are built in React or React Native using `zconnect-js` and `zconnect-web`.

<img style="display: block; margin: 0 auto; width: 800px;" src="/assets/system-diagram.png" alt="Zconnect System Diagram" >

Any of the parts can be used independently of the others, since they interact via simple APIs. However, the components are designed to work together so that you can quickly and easily build and IoT system with an interface made from reusable components.

<a class="btn" href="/apidocs">
  HTTP API specs
</a>
<span class="btn disabled">
  MQTT specs (coming soon)
</span>
<a class="btn" href="/styleguide">
  React Component Guide
</a>

# Core Repositories

## zconnect-django

The core of ZConnect, built with Django for an excellent developer experience.

- manage devices, users and organizations
- provides a complete RESTful HTTP API
- optional modules for billing and time-series data

<a href="https://github.com/zconnect-iot/zconnect-django" class="btn">
  View on GitHub
</a>


## zconnect-js

Provides middleware, actions, selectors and utilities for connecting to ZConnect API. Integrates with the redux store in React and React-Native apps. Consists of:

- custom api interaction layer
- authentication logic

<a class="btn" href="https://github.com/zconnect-iot/zconnect-js">
  View on GitHub
</a>


## zconnect-web

Build ZConnect web-apps faster with a set of intiutive and easy-to-use building
blocks.

- layout components including navbars, interactive panels, forms and controls
- api connected components including time series graphs and device activity streams
- easy theming using scss vars or full customisation with classnames

<a class="btn" href="https://github.com/zconnect-iot/zconnect-web">
  View on GitHub
</a>
<a class="btn" href="/styleguide">
  Component Guide
</a>


# Testing and Demo Repositories


## zconnect-web-template

A "ZConnect Quickstart" designed to make it very easy to get started on a
web-app built with ZConnect.

- demos the usage of the available components
- shows how the style can be customised
- can be used as a starting point for a new project

<a class="btn" href="https://github.com/zconnect-iot/zconnect-web-template">
  View on GitHub
</a>


## zconnect-django-demo

An example IoT platform built on `zconnect-django`.

<a class="btn" href="https://github.com/zconnect-iot/zconnect-django-demo">
  View on GitHub
</a>


## zconnect-system-demo

A complete IoT system demo built using docker.

- an instance of `zconnect-django-demo` built using `zconnect-django`
- an instance of `zconnect-web-tempalte` built using `zconnect-js` and `zconnect-web`
- a device emulator, including a visual front-end to see and set device state
- a mock MQTT broker using `ibm-iot-emulator`

<a class="btn" href="https://github.com/zconnect-iot/zconnect-system-demo">
  View on GitHub
</a>


## ibm-iot-emulator

A mock for the IBM IoT platform for easier testing that doesn't pollute live
data.

- hosts an MQTT broker which acts in the same way as the IBM MQTT broker
- hosts an API which emulates the IBM IoT API
- hosted in a docker container to give high portability.

<a class="btn" href="https://github.com/zconnect-iot/ibm-iot-emulator">
  View on GitHub
</a>


## zconnect-mqtt-auth

A mosquitto Plugin authorising devices used by ibm-iot-emulator

<a class="btn" href="https://github.com/zconnect-iot/zconnect-mqtt-auth">
  View on GitHub
</a>


## device-simulator-frontend

A simple interface which lets you interact with a virtual device that is
connected to the Zconnect platform.

<a class="btn" href="https://github.com/zconnect-iot/device-simulator-frontend">
  View on GitHub
</a>

## device-simulator-backend

A simulated device for use with `device-simlator-frontend`.

<a class="btn" href="https://github.com/zconnect-iot/device-simulator-backend">
  View on GitHub
</a>
