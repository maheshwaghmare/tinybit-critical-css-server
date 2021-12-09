tinybit-critical-css-server
===========================

Standalone service to generate critical CSS, built on [critical](https://github.com/addyosmani/critical).

## Install

### Locally

Run on your local machine:

```bash
git clone git@github.com:pinchofyum/tinybit-critical-css-server.git
cd tinybit-critical-css-server
npm install
npm start
```

### Google Cloud Function

Run as a Google Cloud Function:

1. Create a new Cloud Run Service.
2. Select "Continuously deploy new revisions from a source repository".
3. Fork this repository, then select it as the repository to build.
4. Build type will be "Dockerfile", because Puppeteer requires extra system dependencies.
5. Complete the rest of the Create Service steps. Minimum reqs seem to be 1 GB memory, 2 CPU.

## Usage

tinybit-critical-css-server implements a simple HTTP API.

Simply `POST /` with `html` and `css` to receive `css` in response.
