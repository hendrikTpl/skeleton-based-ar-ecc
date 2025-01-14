# PoseNet Demos

## Contents

### Demo 1: Camera

The camera demo shows how to estimate poses in real-time from a webcam video stream.

<img src="https://raw.githubusercontent.com/tensorflow/tfjs-models/master/posenet/demos/camera.gif" alt="cameraDemo" style="width: 600px;"/>


### Demo 2: Coco Images

The [coco images](http://cocodataset.org/#home) demo shows how to estimate poses in images. It also illustrates the differences between the single-person and multi-person pose detection algorithms.

<img src="https://raw.githubusercontent.com/tensorflow/tfjs-models/master/posenet/demos/coco.gif" alt="cameraDemo" style="width: 600px;"/>


## Setup Dependencies
### Linux
1. Install yarn
```sh
curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | sudo apt-key add -
echo "deb https://dl.yarnpkg.com/debian/ stable main" | sudo tee /etc/apt/sources.list.d/yarn.list

sudo apt update && sudo apt install yarn
```
2. NodeJS and NPM
```sh
tar -xJf node-v#.#.#-linux-arm64.tar.xz
cd node-v#.#.#-linux-arm64
sudo cp -R * /usr/local/
node -v
npm -v
```
## Setup

cd into the demos folder:

```sh
cd posenet/demos
```

Install dependencies and prepare the build directory:

```sh
yarn
```

To watch files for changes, and launch a dev server:

```sh
yarn watch
```

## If you are developing posenet locally, and want to test the changes in the demos

Cd into the posenet folder:
```sh
cd posenet
```

Install dependencies:
```sh
yarn
```

Publish posenet locally:
```sh
yarn build && yarn yalc publish
```

Cd into the demos and install dependencies:

```sh
cd demos
yarn
```

Link the local posenet to the demos:
```sh
yarn yalc link @tensorflow-models/posenet
```

Start the dev demo server:
```sh
yarn watch
```

To get future updates from the posenet source code:
```
# cd up into the posenet directory
cd ../
yarn build && yarn yalc push
```
